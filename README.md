# SendPulse (sendpulse)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SendPulse is a multichannel marketing platform with a unified REST API for email campaigns and address books, SMTP transactional email, SMS, web push notifications, chatbots across messengers, and Automation 360 flows. The API uses OAuth2 client_credentials to issue short-lived Bearer tokens against https://api.sendpulse.com.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sendpulse/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sendpulse/refs/heads/main/apis.yml)

## Tags

- Marketing
- Email
- SMS
- Web Push
- Chatbots
- Transactional Email
- Multichannel

## Timestamps

- **Created:** 2026-06-25
- **Modified:** 2026-06-25

## APIs

### SendPulse Address Books & Email API

Manage mailing lists (address books), subscribers and variables, and create, send, and report on bulk email campaigns, senders, templates, and the email blacklist.

- **Human URL:** [https://sendpulse.com/integrations/api/bulk-email](https://sendpulse.com/integrations/api/bulk-email)
- **Base URL:** `https://api.sendpulse.com`

#### Tags

- Email
- Address Books
- Campaigns

#### Properties

- [Documentation](https://sendpulse.com/integrations/api/bulk-email)
- [API Reference](https://sendpulse.com/integrations/api)
- [OpenAPI](openapi/sendpulse-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sendpulse.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sendpulse.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SendPulse SMTP / Transactional Email API

Send and track transactional email over SMTP, list sent messages, manage sending IP addresses, and maintain the unsubscribe list.

- **Human URL:** [https://sendpulse.com/integrations/api/smtp](https://sendpulse.com/integrations/api/smtp)
- **Base URL:** `https://api.sendpulse.com`

#### Tags

- SMTP
- Transactional Email
- Email

#### Properties

- [Documentation](https://sendpulse.com/integrations/api/smtp)
- [OpenAPI](openapi/sendpulse-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sendpulse.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sendpulse.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SendPulse SMS API

Add and manage phone numbers in address books, send SMS to phone lists, create and cancel SMS campaigns, retrieve campaign cost and statistics, and manage the SMS blacklist.

- **Human URL:** [https://sendpulse.com/integrations/api/bulk-sms](https://sendpulse.com/integrations/api/bulk-sms)
- **Base URL:** `https://api.sendpulse.com`

#### Tags

- SMS
- Messaging
- Campaigns

#### Properties

- [Documentation](https://sendpulse.com/integrations/api/bulk-sms)
- [OpenAPI](openapi/sendpulse-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sendpulse.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sendpulse.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SendPulse Web Push API

Create web push notification campaigns, manage registered websites and their subscribers and variables, retrieve integration code, and pull campaign statistics.

- **Human URL:** [https://sendpulse.com/integrations/api/web-push](https://sendpulse.com/integrations/api/web-push)
- **Base URL:** `https://api.sendpulse.com`

#### Tags

- Web Push
- Notifications
- Subscriptions

#### Properties

- [Documentation](https://sendpulse.com/integrations/api/web-push)
- [OpenAPI](openapi/sendpulse-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sendpulse.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sendpulse.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SendPulse Chatbots API

Manage chatbots across Telegram, Facebook Messenger, WhatsApp, Instagram, Viber, and Live Chat - list bots and contacts, send messages, and run flows.

- **Human URL:** [https://sendpulse.com/integrations/api/chatbot](https://sendpulse.com/integrations/api/chatbot)
- **Base URL:** `https://api.sendpulse.com`

#### Tags

- Chatbots
- Messengers
- Conversational

#### Properties

- [Documentation](https://sendpulse.com/integrations/api/chatbot)
- [OpenAPI](openapi/sendpulse-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sendpulse.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sendpulse.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SendPulse Automation 360 API

Trigger Automation 360 flows by sending events with subscriber data, and report on flow, element, and conversion statistics.

- **Human URL:** [https://sendpulse.com/integrations/api/automation360](https://sendpulse.com/integrations/api/automation360)
- **Base URL:** `https://api.sendpulse.com`

#### Tags

- Automation
- Workflows
- Events

#### Properties

- [Documentation](https://sendpulse.com/integrations/api/automation360)
- [OpenAPI](openapi/sendpulse-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sendpulse.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sendpulse.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/sendpulse)
- [LinkedIn](https://www.linkedin.com/company/sendpulse)
- [Website](https://sendpulse.com/)
- [Documentation](https://sendpulse.com/integrations/api)
- [Plans](plans/sendpulse-plans-pricing.yml)
- [Rate Limits](rate-limits/sendpulse-rate-limits.yml)
- [Fin Ops](finops/sendpulse-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
