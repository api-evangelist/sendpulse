---
name: sendpulse-transactional-smtp
description: Send transactional email through the SendPulse SMTP API and reconcile delivery, bounces and unsubscribes.
api: SendPulse SMTP API
spec: openapi/sendpulse-smtp-openapi.yml
base_url: https://api.sendpulse.com
generated: '2026-08-13'
method: generated
source: openapi/sendpulse-smtp-openapi.yml + https://sendpulse.com/integrations/api/smtp
operations:
  - getSmtpSenders
  - addSmtpSender
  - getSmtpAllowedDomains
  - addSmtpDomain
  - sendSmtpEmail
  - getSmtpEmailInfo
  - getSmtpEmails
  - getSmtpEmailsBatchInfo
  - getSmtpEmailsTotal
  - getSmtpBouncesDay
  - getSmtpBouncesTotal
  - searchSmtpUnsubscribe
  - unsubscribeSmtpRecipients
  - resubscribeSmtpRecipient
  - getSmtpIps
---

# Send transactional email with SendPulse SMTP

Base `https://api.sendpulse.com`, `Authorization: Bearer <token>`.

## Steps

1. **Check sender identity is ready.** `getSmtpSenders` (`GET /smtp/senders`) and
   `getSmtpAllowedDomains` (`GET /v2/email-service/smtp/sender_domains`). Add what is
   missing with `addSmtpSender` (`POST /senders`) or `addSmtpDomain`
   (`POST /v2/email-service/smtp/sender_domains/{domain}`). Error `400` means the SMTP
   account does not exist yet — create it in the account before calling the API.
2. **Respect the recipient's state before sending.** `searchSmtpUnsubscribe`
   (`GET /smtp/unsubscribe/search`) tells you whether the address has opted out.
   Sending to an opted-out or blacklisted address is a compliance failure, not a retry.
3. **Send.** `sendSmtpEmail` (`POST /smtp/emails`).
4. **Reconcile, do not assume.** `getSmtpEmailInfo` (`GET /smtp/emails/{id}`) for one
   message, `getSmtpEmailsBatchInfo` (`POST /smtp/emails/info`) for many,
   `getSmtpEmails` (`GET /smtp/emails`) and `getSmtpEmailsTotal`
   (`GET /smtp/emails/total`) for a window.
5. **Watch deliverability.** `getSmtpBouncesDay` (`GET /smtp/bounces/day`) and
   `getSmtpBouncesTotal` (`GET /smtp/bounces/day/total`). `getSmtpIps` (`GET /smtp/ips`)
   lists the sending IPs.
6. **Honour opt-outs.** `unsubscribeSmtpRecipients` (`POST /smtp/unsubscribe`),
   `resubscribeSmtpRecipient` (`POST /smtp/resubscribe`), and `removeSmtpUnsubscribe`
   (`DELETE /smtp/unsubscribe`) only on an explicit human instruction.

## Rules that will bite you

- **`POST /smtp/emails` has no idempotency key.** A timeout is ambiguous. Reconcile with
  `getSmtpEmails` over the send window before re-sending, or you will double-send.
- 10 requests/second hard ceiling (error `2020202020`); plan quota exhaustion returns `429`
  with no `Retry-After` and no `RateLimit-*` headers.
- Error `904` is a blacklisted address, `906` a syntax error, `905` a sender quota — none
  of these are retryable.
- `403` means the plan or role forbids the operation, not that the token is bad; `401` is
  the expired-token case.
