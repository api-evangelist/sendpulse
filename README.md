# SendPulse

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

SendPulse is a multichannel marketing automation platform covering bulk email, SMTP transactional email, SMS, web push, website pop-ups, a CRM, an online course builder, and chatbots across WhatsApp, Telegram, Facebook Messenger, Instagram, Viber, TikTok and its own live chat widget. It publishes nineteen first-party OpenAPI 3.1 specifications totalling 635 operations from https://api.sendpulse.com/.well-known/openapi/, indexed by a master index.yaml and mirrored by an llms.txt, an llms-full.txt, a service-directory.json and an ai-plugin.json. Authentication is OAuth 2.0 client_credentials against POST /oauth/access_token (one-hour Bearer tokens) or a static account API key in the same Authorization header. SendPulse also operates a first-party remote MCP server at https://mcp.sendpulse.com/mcp with 147 published tools covering chatbots, CRM, courses, email and SMTP.

**Areas:** Marketing · Marketing Automation · Email · Transactional Email · SMS · Web Push · Chatbots · CRM · Multi-Channel · Messaging · Online Courses · Popups

## SendPulse on APIs.io

Everything profiled for SendPulse is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/sendpulse/](https://apis.io/providers/sendpulse/)** — or go straight to one of the APIs or properties below.

### APIs (85)

- [SendPulse Account API](https://apis.io/apis/sendpulse/sendpulse-account-api/) — The account API from SendPulse — 1 operation(s) for account.
- [SendPulse Attachments API](https://apis.io/apis/sendpulse/sendpulse-attachments-api/) — The Attachments API from SendPulse — 3 operation(s) for attachments.
- [SendPulse Automation Flows API](https://apis.io/apis/sendpulse/sendpulse-automation-flows-api/) — Endpoints related to Automation Flows.
- [SendPulse Balance API](https://apis.io/apis/sendpulse/sendpulse-balance-api/) — Endpoints related to Balance.
- [SendPulse Blacklist API](https://apis.io/apis/sendpulse/sendpulse-blacklist-api/) — Endpoints related to Blacklist.
- [SendPulse Board attributes API](https://apis.io/apis/sendpulse/sendpulse-board-attributes-api/) — The Board attributes API from SendPulse — 2 operation(s) for board attributes.
- [SendPulse Bots API](https://apis.io/apis/sendpulse/sendpulse-bots-api/) — The bots API from SendPulse — 2 operation(s) for bots.
- [SendPulse Bounces API](https://apis.io/apis/sendpulse/sendpulse-bounces-api/) — The Bounces API from SendPulse — 2 operation(s) for bounces.
- [SendPulse Campaigns API](https://apis.io/apis/sendpulse/sendpulse-campaigns-api/) — Endpoints related to Campaigns.
- [SendPulse Chats API](https://apis.io/apis/sendpulse/sendpulse-chats-api/) — The chats API from SendPulse — 3 operation(s) for chats.
- [SendPulse Checklist Items API](https://apis.io/apis/sendpulse/sendpulse-checklist-items-api/) — The Checklist Items API from SendPulse — 2 operation(s) for checklist items.
- [SendPulse Company API](https://apis.io/apis/sendpulse/sendpulse-company-api/) — The Company API from SendPulse — 4 operation(s) for company.
- [SendPulse Company Attributes API](https://apis.io/apis/sendpulse/sendpulse-company-attributes-api/) — The Company Attributes API from SendPulse — 2 operation(s) for company attributes.
- [SendPulse Company history API](https://apis.io/apis/sendpulse/sendpulse-company-history-api/) — The Company history API from SendPulse — 1 operation(s) for company history.
- [SendPulse Compliance API](https://apis.io/apis/sendpulse/sendpulse-compliance-api/) — The Compliance API from SendPulse — 2 operation(s) for compliance.
- [SendPulse Configuration API](https://apis.io/apis/sendpulse/sendpulse-configuration-api/) — The Configuration API from SendPulse — 9 operation(s) for configuration.
- [SendPulse Contact Attributes API](https://apis.io/apis/sendpulse/sendpulse-contact-attributes-api/) — The Contact Attributes API from SendPulse — 2 operation(s) for contact attributes.
- [SendPulse Contact attributes Value API](https://apis.io/apis/sendpulse/sendpulse-contact-attributes-value-api/) — The Contact attributes Value API from SendPulse — 2 operation(s) for contact attributes value.
- [SendPulse Contact Attributes Values API](https://apis.io/apis/sendpulse/sendpulse-contact-attributes-values-api/) — The Contact Attributes Values API from SendPulse — 1 operation(s) for contact attributes values.
- [SendPulse Contact email addresses API](https://apis.io/apis/sendpulse/sendpulse-contact-email-addresses-api/) — The Contact email addresses API from SendPulse — 2 operation(s) for contact email addresses.
- [SendPulse Contact history API](https://apis.io/apis/sendpulse/sendpulse-contact-history-api/) — The Contact history API from SendPulse — 1 operation(s) for contact history.
- [SendPulse Contact phone number API](https://apis.io/apis/sendpulse/sendpulse-contact-phone-number-api/) — The Contact phone number API from SendPulse — 2 operation(s) for contact phone number.
- [SendPulse Contact tags API](https://apis.io/apis/sendpulse/sendpulse-contact-tags-api/) — The Contact tags API from SendPulse — 3 operation(s) for contact tags.
- [SendPulse Contacts API](https://apis.io/apis/sendpulse/sendpulse-contacts-api/) — The Contacts API from SendPulse — 51 operation(s) for contacts.
- [SendPulse Contacts messengers API](https://apis.io/apis/sendpulse/sendpulse-contacts-messengers-api/) — The Contacts messengers API from SendPulse — 2 operation(s) for contacts messengers.
- [SendPulse Conversions API](https://apis.io/apis/sendpulse/sendpulse-conversions-api/) — Endpoints related to Conversions.
- [SendPulse Course tariffs API](https://apis.io/apis/sendpulse/sendpulse-course-tariffs-api/) — The Course tariffs API from SendPulse — 1 operation(s) for course tariffs.
- [SendPulse Courses API](https://apis.io/apis/sendpulse/sendpulse-courses-api/) — The Courses API from SendPulse — 1 operation(s) for courses.
- [SendPulse Custom Tab API](https://apis.io/apis/sendpulse/sendpulse-custom-tab-api/) — The Custom Tab API from SendPulse — 3 operation(s) for custom tab.
- [SendPulse Deal attribute Value API](https://apis.io/apis/sendpulse/sendpulse-deal-attribute-value-api/) — The Deal attribute Value API from SendPulse — 3 operation(s) for deal attribute value.
- [SendPulse Deal Attributes API](https://apis.io/apis/sendpulse/sendpulse-deal-attributes-api/) — The Deal Attributes API from SendPulse — 3 operation(s) for deal attributes.
- [SendPulse Deal contacts API](https://apis.io/apis/sendpulse/sendpulse-deal-contacts-api/) — The Deal contacts API from SendPulse — 2 operation(s) for deal contacts.
- [SendPulse Deal Expiration API](https://apis.io/apis/sendpulse/sendpulse-deal-expiration-api/) — The Deal Expiration API from SendPulse — 1 operation(s) for deal expiration.
- [SendPulse Deal history API](https://apis.io/apis/sendpulse/sendpulse-deal-history-api/) — The Deal history API from SendPulse — 1 operation(s) for deal history.
- [SendPulse Deal notes API](https://apis.io/apis/sendpulse/sendpulse-deal-notes-api/) — The Deal notes API from SendPulse — 2 operation(s) for deal notes.
- [SendPulse Deals API](https://apis.io/apis/sendpulse/sendpulse-deals-api/) — The Deals API from SendPulse — 4 operation(s) for deals.
- [SendPulse Dialogs API](https://apis.io/apis/sendpulse/sendpulse-dialogs-api/) — The dialogs API from SendPulse — 1 operation(s) for dialogs.
- [SendPulse Directory API](https://apis.io/apis/sendpulse/sendpulse-directory-api/) — directory entity
- [SendPulse ECommerce Product API](https://apis.io/apis/sendpulse/sendpulse-ecommerce-product-api/) — The ECommerce Product API from SendPulse — 14 operation(s) for ecommerce product.
- [SendPulse Element Statistics API](https://apis.io/apis/sendpulse/sendpulse-element-statistics-api/) — Endpoints related to Element Statistics.
- [SendPulse Email address API](https://apis.io/apis/sendpulse/sendpulse-email-address-api/) — Endpoints related to Email address.
- [SendPulse Emails API](https://apis.io/apis/sendpulse/sendpulse-emails-api/) — The Emails API from SendPulse — 7 operation(s) for emails.
- [SendPulse Events API](https://apis.io/apis/sendpulse/sendpulse-events-api/) — Endpoints related to Events.
- [SendPulse File API](https://apis.io/apis/sendpulse/sendpulse-file-api/) — file entity
- [SendPulse File Manager API](https://apis.io/apis/sendpulse/sendpulse-file-manager-api/) — The File Manager API from SendPulse — 1 operation(s) for file manager.
- [SendPulse Flows API](https://apis.io/apis/sendpulse/sendpulse-flows-api/) — The flows API from SendPulse — 3 operation(s) for flows.
- [SendPulse Mailing List Verification API](https://apis.io/apis/sendpulse/sendpulse-mailing-list-verification-api/) — Endpoints related to Mailing List Verification.
- [SendPulse Mailing lists API](https://apis.io/apis/sendpulse/sendpulse-mailing-lists-api/) — Endpoints related to Mailing lists.
- [SendPulse Manager Settings API](https://apis.io/apis/sendpulse/sendpulse-managersettings-api/) — The ManagerSettings API from SendPulse — 5 operation(s) for managersettings.
- [SendPulse Messengers API](https://apis.io/apis/sendpulse/sendpulse-messengers-api/) — The messengers API from SendPulse — 3 operation(s) for messengers.
- [SendPulse Messengers types API](https://apis.io/apis/sendpulse/sendpulse-messengers-types-api/) — The Messengers types API from SendPulse — 1 operation(s) for messengers types.
- [SendPulse Payments API](https://apis.io/apis/sendpulse/sendpulse-payments-api/) — The Payments API from SendPulse — 6 operation(s) for payments.
- [SendPulse Phones API](https://apis.io/apis/sendpulse/sendpulse-phones-api/) — The Phones API from SendPulse — 3 operation(s) for phones.
- [SendPulse Pipeline Steps API](https://apis.io/apis/sendpulse/sendpulse-pipeline-steps-api/) — The Pipeline Steps API from SendPulse — 2 operation(s) for pipeline steps.
- [SendPulse Pipelines API](https://apis.io/apis/sendpulse/sendpulse-pipelines-api/) — The Pipelines API from SendPulse — 2 operation(s) for pipelines.
- [SendPulse Popup API](https://apis.io/apis/sendpulse/sendpulse-popup-api/) — The Popup API from SendPulse — 5 operation(s) for popup.
- [SendPulse Popup statistic API](https://apis.io/apis/sendpulse/sendpulse-popup-statistic-api/) — The Popup statistic API from SendPulse — 3 operation(s) for popup statistic.
- [SendPulse Project API](https://apis.io/apis/sendpulse/sendpulse-project-api/) — The Project API from SendPulse — 2 operation(s) for project.
- [SendPulse Project statistic API](https://apis.io/apis/sendpulse/sendpulse-project-statistic-api/) — The Project statistic API from SendPulse — 1 operation(s) for project statistic.
- [SendPulse Reports API](https://apis.io/apis/sendpulse/sendpulse-reports-api/) — Endpoints related to Reports.
- [SendPulse Schools API](https://apis.io/apis/sendpulse/sendpulse-schools-api/) — The Schools API from SendPulse — 1 operation(s) for schools.
- [SendPulse Senders API](https://apis.io/apis/sendpulse/sendpulse-senders-api/) — Endpoints related to Senders.
- [SendPulse Single Email Verification API](https://apis.io/apis/sendpulse/sendpulse-single-email-verification-api/) — Endpoints related to Single Email Verification.
- [SendPulse Students API](https://apis.io/apis/sendpulse/sendpulse-students-api/) — The Students API from SendPulse — 7 operation(s) for students.
- [SendPulse Students groups API](https://apis.io/apis/sendpulse/sendpulse-students-groups-api/) — The Students groups API from SendPulse — 1 operation(s) for students groups.
- [SendPulse Subscribers API](https://apis.io/apis/sendpulse/sendpulse-subscribers-api/) — The Subscribers API from SendPulse — 6 operation(s) for subscribers.
- [SendPulse Tags API](https://apis.io/apis/sendpulse/sendpulse-tags-api/) — Endpoints related to Tags.
- [SendPulse Tariff API](https://apis.io/apis/sendpulse/sendpulse-tariff-api/) — The Tariff API from SendPulse — 1 operation(s) for tariff.
- [SendPulse Task Attributes API](https://apis.io/apis/sendpulse/sendpulse-task-attributes-api/) — The Task Attributes API from SendPulse — 2 operation(s) for task attributes.
- [SendPulse Task Checklist API](https://apis.io/apis/sendpulse/sendpulse-task-checklist-api/) — The Task Checklist API from SendPulse — 4 operation(s) for task checklist.
- [SendPulse Task Comments API](https://apis.io/apis/sendpulse/sendpulse-task-comments-api/) — The Task Comments API from SendPulse — 2 operation(s) for task comments.
- [SendPulse Task Entity API](https://apis.io/apis/sendpulse/sendpulse-task-entity-api/) — The Task Entity API from SendPulse — 4 operation(s) for task entity.
- [SendPulse Task history API](https://apis.io/apis/sendpulse/sendpulse-task-history-api/) — The Task history API from SendPulse — 1 operation(s) for task history.
- [SendPulse Task Tags API](https://apis.io/apis/sendpulse/sendpulse-task-tags-api/) — The Task Tags API from SendPulse — 3 operation(s) for task tags.
- [SendPulse Tasks API](https://apis.io/apis/sendpulse/sendpulse-tasks-api/) — The Tasks API from SendPulse — 6 operation(s) for tasks.
- [SendPulse Tasks boards API](https://apis.io/apis/sendpulse/sendpulse-tasks-boards-api/) — The Tasks boards API from SendPulse — 2 operation(s) for tasks boards.
- [SendPulse Tasks steps API](https://apis.io/apis/sendpulse/sendpulse-tasks-steps-api/) — The Tasks steps API from SendPulse — 2 operation(s) for tasks steps.
- [SendPulse Telephony API](https://apis.io/apis/sendpulse/sendpulse-telephony-api/) — The Telephony API from SendPulse — 4 operation(s) for telephony.
- [SendPulse Templates API](https://apis.io/apis/sendpulse/sendpulse-templates-api/) — Endpoints related to Templates.
- [SendPulse Triggers API](https://apis.io/apis/sendpulse/sendpulse-triggers-api/) — (keywords)
- [SendPulse Unsubscribe API](https://apis.io/apis/sendpulse/sendpulse-unsubscribe-api/) — The Unsubscribe API from SendPulse — 3 operation(s) for unsubscribe.
- [SendPulse Users API](https://apis.io/apis/sendpulse/sendpulse-users-api/) — The Users API from SendPulse — 1 operation(s) for users.
- [SendPulse Variables API](https://apis.io/apis/sendpulse/sendpulse-variables-api/) — The variables API from SendPulse — 1 operation(s) for variables.
- [SendPulse Webhooks API](https://apis.io/apis/sendpulse/sendpulse-webhooks-api/) — Endpoints related to Webhooks.
- [SendPulse Websites API](https://apis.io/apis/sendpulse/sendpulse-websites-api/) — The Websites API from SendPulse — 4 operation(s) for websites.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Sendpulse Webhooks](https://apis.io/asyncapis/sendpulse/sendpulse-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [SendPulse MCP Server](https://apis.io/servers/sendpulse/sendpulse-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Sendpulse Agentic Access](https://apis.io/agentic-access/sendpulse/sendpulse-agentic-access/)

#### Collections (11)

Postman and Open Collection request collections.

- [SendPulse API](https://apis.io/collections/sendpulse/open-sendpulse/)
- [SendPulse Account API](https://apis.io/collections/sendpulse/open-sendpulse-account-api/)
- [SendPulse Account Address Books API](https://apis.io/collections/sendpulse/open-sendpulse-address-books-api/)
- [SendPulse Account Authorization API](https://apis.io/collections/sendpulse/open-sendpulse-authorization-api/)
- [SendPulse Account Automation 360 API](https://apis.io/collections/sendpulse/open-sendpulse-automation-360-api/)
- [SendPulse Account Email Blacklist API](https://apis.io/collections/sendpulse/open-sendpulse-email-blacklist-api/)
- [SendPulse Account Email Campaigns API](https://apis.io/collections/sendpulse/open-sendpulse-email-campaigns-api/)
- [SendPulse Account Senders API](https://apis.io/collections/sendpulse/open-sendpulse-senders-api/)
- [SendPulse Account SMS API](https://apis.io/collections/sendpulse/open-sendpulse-sms-api/)
- [SendPulse Account SMTP API](https://apis.io/collections/sendpulse/open-sendpulse-smtp-api/)
- [SendPulse Account Web Push API](https://apis.io/collections/sendpulse/open-sendpulse-web-push-api/)

#### Overlays (104)

OpenAPI overlays, including conversational phrasing for each operation.

- [Sendpulse A360 Overlay](https://apis.io/overlays/sendpulse/sendpulse-a360-overlay/)
- [Sendpulse Account Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-account-api-phrasing-overlay/)
- [Sendpulse Attachments Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-attachments-api-phrasing-overlay/)
- [Sendpulse Automation Flows Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-automation-flows-api-phrasing-overlay/)
- [Sendpulse Balance Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-balance-api-phrasing-overlay/)
- [Sendpulse Blacklist Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-blacklist-api-phrasing-overlay/)
- [Sendpulse Board Attributes Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-board-attributes-api-phrasing-overlay/)
- [Sendpulse Bots Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-bots-api-phrasing-overlay/)
- [Sendpulse Bounces Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-bounces-api-phrasing-overlay/)
- [Sendpulse Bulk Email Overlay](https://apis.io/overlays/sendpulse/sendpulse-bulk-email-overlay/)
- [Sendpulse Campaigns Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-campaigns-api-phrasing-overlay/)
- [Sendpulse Chatbots Overlay](https://apis.io/overlays/sendpulse/sendpulse-chatbots-overlay/)
- [Sendpulse Chats Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-chats-api-phrasing-overlay/)
- [Sendpulse Checklist Items Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-checklist-items-api-phrasing-overlay/)
- [Sendpulse Company Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-company-api-phrasing-overlay/)
- [Sendpulse Company Attributes Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-company-attributes-api-phrasing-overlay/)
- [Sendpulse Company History Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-company-history-api-phrasing-overlay/)
- [Sendpulse Compliance Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-compliance-api-phrasing-overlay/)
- [Sendpulse Configuration Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-configuration-api-phrasing-overlay/)
- [Sendpulse Contact Attributes Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-contact-attributes-api-phrasing-overlay/)
- [Sendpulse Contact Attributes Value Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-contact-attributes-value-api-phrasing-overlay/)
- [Sendpulse Contact Attributes Values Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-contact-attributes-values-api-phrasing-overlay/)
- [Sendpulse Contact Email Addresses Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-contact-email-addresses-api-phrasing-overlay/)
- [Sendpulse Contact History Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-contact-history-api-phrasing-overlay/)
- [Sendpulse Contact Phone Number Api Phrasing Overlay](https://apis.io/overlays/sendpulse/sendpulse-contact-phone-number-api-phrasing-overlay/)
- …and 79 more published on APIs.io

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Sendpulse Authentication](https://apis.io/security/sendpulse/sendpulse-authentication/)
- [Sendpulse Domain Security](https://apis.io/security/sendpulse/sendpulse-domain-security/)
- [Sendpulse Trust Center](https://apis.io/security/sendpulse/sendpulse-trust-center/)
- [Sendpulse Vulnerability Disclosure](https://apis.io/security/sendpulse/sendpulse-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Sendpulse Scopes](https://apis.io/scopes/sendpulse/sendpulse-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Sendpulse Plans Pricing](https://apis.io/plans/sendpulse/sendpulse-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Sendpulse Rate Limits](https://apis.io/rate-limits/sendpulse/sendpulse-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Sendpulse Finops](https://apis.io/finops/sendpulse/sendpulse-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://sendpulse.com/)
- [Documentation](https://sendpulse.com/integrations/api)
- [Getting started](https://sendpulse.com/integrations/api)
- [API reference](https://sendpulse.com/integrations/api/bulk-email)
- [Pricing](https://sendpulse.com/prices)
- [Sign up](https://sendpulse.com/register)
- [Support](https://sendpulse.com/knowledge-base)
- [Changelog](https://sendpulse.com/updates)
- [Blog](https://sendpulse.com/blog)
- [Terms of service](https://sendpulse.com/legal/terms)
- [Privacy policy](https://sendpulse.com/legal/pp)
- [GitHub](https://github.com/sendpulse)
- [Status](https://status.sendpulse.com/)

## API Evangelist rating

**Kin Score 68.4** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 52.7 |
| Contract governance | 4.5 |
| Operational transparency | 81.6 |
| Developer ergonomics | 66.1 |
| Access clarity | 88.9 |

**Agent readiness 51.7** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly (partial credit) |

**Regulatory alignment 44.2** — Telecommunications

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/sendpulse/](https://apis.io/providers/sendpulse/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for SendPulse: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/sendpulse/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
