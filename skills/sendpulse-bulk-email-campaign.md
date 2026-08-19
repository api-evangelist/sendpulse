---
name: sendpulse-bulk-email-campaign
description: Build a SendPulse mailing list, load contacts, verify a sender, price the send, launch a bulk email campaign and read its statistics.
api: SendPulse Bulk Email API
spec: openapi/sendpulse-bulk-email-openapi.yml
base_url: https://api.sendpulse.com
generated: '2026-08-13'
method: generated
source: openapi/sendpulse-bulk-email-openapi.yml + https://sendpulse.com/integrations/api/bulk-email
operations:
  - createMailingList
  - addEmailsToMailingList
  - getEmailsTotalCount
  - getSenders
  - addSender
  - requestSenderActivationCode
  - activateSender
  - getCampaignCostByList
  - createCampaign
  - getCampaignById
  - getCampaignCountryStats
  - getCampaignsByList
  - cancelCampaign
---

# Send a bulk email campaign with SendPulse

All calls go to `https://api.sendpulse.com` with `Authorization: Bearer <token>`.

## Before you start

1. Get a token. `POST https://api.sendpulse.com/oauth/access_token` with
   `{"grant_type":"client_credentials","client_id":"...","client_secret":"..."}`.
   The token lasts **3600 seconds** — refresh before it expires. A static API key from
   account settings works in the same `Authorization: Bearer` header and never expires.
   Note: the token endpoint is **not** declared in any published OpenAPI spec, only in the docs.
2. Confirm you have budget: `getBalance` (`GET /balance`) or `getDetailedBalance`
   (`GET /user/balance/detail`). Error code `707` means the balance is depleted.

## Steps

1. **Create the list** — `createMailingList` (`POST /addressbooks`). Error `203` means the
   name already exists; reuse the existing list via `getMailingLists` instead of retrying.
2. **Load contacts** — `addEmailsToMailingList` (`POST /addressbooks/{id}/emails`).
   Confirm the load with `getEmailsTotalCount` (`GET /addressbooks/{id}/emails/total`)
   rather than assuming success.
3. **Have a verified sender** — `getSenders` (`GET /senders`). If the address you need is
   missing, `addSender` (`POST /senders`), then `requestSenderActivationCode`
   (`GET /senders/{email}/code`) and `activateSender` (`POST /senders/{email}/code`).
   Error `1004` means a code was already sent — wait 15 minutes, do not retry in a loop.
4. **Price the send** — `getCampaignCostByList` (`GET /addressbooks/{id}/cost`) before
   committing. Stop and report to the human if the cost is unexpected.
5. **Launch** — `createCampaign` (`POST /campaigns`). Error `708` means the recipient count
   exceeds the plan; `720`/`721` mean an empty subject or body.
6. **Read results** — `getCampaignById` (`GET /campaigns/{id}`),
   `getCampaignCountryStats` (`GET /campaigns/{id}/countries`), and
   `getCampaignsByList` (`GET /addressbooks/{id}/campaigns`).
   Cancel a scheduled send with `cancelCampaign` (`DELETE /campaigns/{id}`).

## Rules that will bite you

- **There is no idempotency key.** `POST /campaigns` is not safe to retry. On a timeout,
  call `getCampaignsByList` and look for the campaign before sending again.
- **Only 4 API campaigns per hour.** Error `791` is that limit, not a transient failure.
- **Hard ceiling of 10 requests/second** — error code `2020202020`. Plan quotas are
  1,000/min (Free), 2,000/min (Standard), 3,000/min (Enterprise); exhaustion returns `429`.
- **No rate-limit headers exist.** You cannot read remaining quota; back off on `429` blind.
- Pagination here is `limit` + `offset`, e.g. `GET /addressbooks?limit=10&offset=5`.
  Other SendPulse services use `size`/`skip` or `search_after` — do not carry the idiom across.
- Errors are `{"message": "...", "error_code": <int>}`, not RFC 9457. See
  `errors/sendpulse-problem-types.yml` for the full code registry.
