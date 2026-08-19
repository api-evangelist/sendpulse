---
name: sendpulse-whatsapp-chatbot-messaging
description: Find a WhatsApp chatbot contact, send a session message or an approved template, tag them, and run a flow — with the SendPulse chatbot conventions that differ from the email API.
api: WhatsApp service API
spec: openapi/sendpulse-whatsapp-openapi.yml
base_url: https://api.sendpulse.com/whatsapp
generated: '2026-08-13'
method: generated
source: openapi/sendpulse-whatsapp-openapi.yml
operations:
  - getContactByPhone
  - getContactById
  - getContactsByTag
  - getContactsByVariable
  - createContact
  - sendContactMessage
  - sendMessageToContactByPhone
  - sendTemplateToContact
  - sendTemplateByPhone
  - setContactVariable
  - setContactTag
  - createContactNote
  - setPauseAutomation
  - markContactMessagesAsRead
---

# Message a WhatsApp chatbot contact with SendPulse

Base `https://api.sendpulse.com/whatsapp` — every messenger channel has its own host path
(`/telegram`, `/messenger` for Facebook, `/instagram`, `/tiktok`, `/live-chat`,
`/viber/chatbots`) and the six sibling specs share this shape almost operation for operation.

## Steps

1. **Resolve the contact first.** `getContactByPhone` (`GET /contacts/getByPhone`) or
   `getContactById` (`GET /contacts/get`). Chatbot contact IDs are 24-character hex strings
   (e.g. `6930338aae1f752ca105943f`), not integers like the email service uses.
   Segment with `getContactsByTag` (`GET /contacts/getByTag`) or `getContactsByVariable`
   (`GET /contacts/getByVariable`).
2. **Choose session message vs template.** Inside an open conversation window use
   `sendContactMessage` (`POST /contacts/send`) or `sendMessageToContactByPhone`
   (`POST /contacts/sendByPhone`). Outside it you must use a **pre-approved WhatsApp
   Business template**: `sendTemplateToContact` (`POST /contacts/sendTemplate`) or
   `sendTemplateByPhone` (`POST /contacts/sendTemplateByPhone`). Do not attempt a free-form
   send outside the window and treat the failure as transient — it is a policy refusal.
3. **Enrich.** `setContactVariable` (`POST /contacts/setVariable`), `setContactTag`
   (`POST /contacts/setTag`), `createContactNote` (`POST /contacts/createNote`).
4. **Control automation.** `setPauseAutomation` (`POST /contacts/setPauseAutomation`)
   before a human takeover, so a flow does not talk over the operator.
5. **Tidy the inbox.** `markContactMessagesAsRead` (`PUT /contacts/mark-read`).

## Rules that will bite you

- Nearly every mutation here is a **`POST` with the verb in the path** (`/contacts/delete`,
  `/contacts/setTag`). There is no REST verb semantics to lean on — read the operationId.
- **Pagination is `size`/`skip`** in the chatbot specs, not `limit`/`offset`.
- No idempotency key: sending twice sends twice. Reconcile before retrying a send.
- The chatbot specs are declared `info.version: 0.0.1`.
- 10 requests/second ceiling (error `2020202020`); `429` on plan quota exhaustion, with no
  `Retry-After` header to read.
