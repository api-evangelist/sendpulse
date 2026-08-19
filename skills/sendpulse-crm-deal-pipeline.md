---
name: sendpulse-crm-deal-pipeline
description: Drive a deal through a SendPulse CRM pipeline — create the pipeline and its stages, create the deal, attach contacts and comments, and move it between stages.
api: SendPulse CRM Public API
spec: openapi/sendpulse-crm-openapi.yml
base_url: https://api.sendpulse.com/crm/v1
generated: '2026-08-13'
method: generated
source: openapi/sendpulse-crm-openapi.yml
operations:
  - getPipelines
  - createPipeline
  - getPipelineById
  - createPipelineStep
  - getPipelineSteps
  - createDeal
  - getDealsList
  - getDeal
  - updateDealById
  - changeDealPipeline
  - getDealContacts
  - addContactToDeal
  - addDealComment
  - getDealComments
  - listPipelineAttributes
  - addDealAttribute
---

# Move a deal through a SendPulse CRM pipeline

Base `https://api.sendpulse.com/crm/v1` — note the **`/crm/v1` prefix**; the email and SMTP
services are unversioned on the bare host. `Authorization: Bearer <token>`.

## Steps

1. **Find or create the pipeline.** `getPipelines` (`GET /pipelines`), then
   `createPipeline` (`POST /pipelines`) only if nothing matches. Read one back with
   `getPipelineById` (`GET /pipelines/{pipelineId}`).
2. **Make sure the stages exist.** `getPipelineSteps` (`GET /pipelines/{pipelineId}/steps`),
   `createPipelineStep` (`POST /pipelines/{pipelineId}/steps`). Deals reference stages by
   ID, so resolve the stage ID before creating a deal — never guess it from a stage name.
3. **Create the deal.** `createDeal` (`POST /deals`) with the pipeline and stage IDs.
4. **Attach the people.** `addContactToDeal`
   (`POST /deals/{dealId}/contacts/{contactId}`); read back with `getDealContacts`
   (`GET /deals/{dealId}/contacts`).
5. **Record context.** `addDealComment` (`POST /deals/{dealId}/comments`),
   `getDealComments` (`GET /deals/{dealId}/comments`).
6. **Custom fields.** `listPipelineAttributes`
   (`GET /pipelines/{pipelineId}/attributes`) then `addDealAttribute`
   (`POST /deals/{dealId}/attributes`).
7. **Progress it.** `updateDealById` (`PUT /deals/{dealId}`) for amount/stage inside the
   same pipeline; `changeDealPipeline` (`POST /deals/{dealId}/change-pipeline`) to move it
   to a different pipeline.

## Rules that will bite you

- **Listing deals is a POST.** `getDealsList` is `POST /deals/get-list`, not a GET. Do not
  treat it as unsafe just because it is a POST, and do not look for a GET that isn't there.
- **No idempotency key.** The spec's own agent instructions say to check for an existing
  record first "to prevent duplicate entries if the API does not handle idempotency."
  Do exactly that before every create.
- CRM paginates with **`search_after`** (cursor) on some list operations and `start`/`limit`
  on others — read the operation's own parameters, do not assume `limit`/`offset`.
- The CRM spec is declared `info.version: 0.1.0`. Treat the contract as pre-1.0.
- Errors are `{"message": "...", "error_code": <int>}`; `403` is a plan/role refusal.
