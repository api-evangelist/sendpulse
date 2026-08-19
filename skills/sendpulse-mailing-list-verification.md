---
name: sendpulse-mailing-list-verification
description: Clean a SendPulse mailing list with the Verifier API before a send — submit the list, poll progress, read results and pull the report.
api: SendPulse Verifier API
spec: openapi/sendpulse-verifier-openapi.yml
base_url: https://api.sendpulse.com
generated: '2026-08-13'
method: generated
source: openapi/sendpulse-verifier-openapi.yml
operations:
  - verifyMailingList
  - getVerificationProgress
  - getVerificationResults
  - getVerifiedLists
  - verifySingleEmail
  - getSingleVerificationResult
  - createVerificationReport
  - viewVerificationReport
  - downloadVerificationReport
---

# Verify a mailing list before sending

Base `https://api.sendpulse.com`, `Authorization: Bearer <token>`.

## Steps

1. **Submit the list.** `verifyMailingList`
   (`POST /verifier-service/send-list-to-verify`) with the address book ID.
   For one address, `verifySingleEmail` (`POST /verifier-service/send-single-to-verify`).
2. **Poll, do not busy-wait.** `getVerificationProgress`
   (`GET /verifier-service/get-progress`). Verification is asynchronous. Keep polling well
   under the 10 requests/second ceiling — back off to seconds, not milliseconds.
3. **Read the outcome.** `getVerificationResults` (`GET /verifier-service/check`), or
   `getSingleVerificationResult` (`GET /verifier-service/get-single-result`).
   `getVerifiedLists` (`GET /verifier-service/check-list`) shows everything verified so far.
4. **Report.** `createVerificationReport` (`POST /verifier-service/make-report`), then
   `viewVerificationReport` (`GET /verifier-service/check-report`) and
   `downloadVerificationReport` (`GET /verifier-service/get-report`).
5. **Then send.** Feed the cleaned list into `sendpulse-bulk-email-campaign`.

## Rules that will bite you

- Verification quota is per plan (100 verifications on Standard, 1,000 on Pro). Running out
  is a plan limit, not an API error to retry.
- Do not re-submit a list that is already in progress — there is no idempotency key and no
  dedupe; check `getVerificationProgress` first.
- Nothing in the spec declares a `429` response even though the documented quota returns one.
