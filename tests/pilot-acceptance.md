# Delivery 1 browser pilot acceptance tests

**Artifact ID:** EXK-TEST-01
**Status:** Not executed. This file is a **test specification**, not test evidence.

## Browser verification matrix
| ID | Scenario | Pass condition |
|---|---|---|
| FB-01 | Secure Cloud Browser login | Authenticated facebook.com loads; no password entered in chat |
| FB-02 | Group/Page administration | Work can find/manage intended group under approved identity |
| FB-03 | Test post | Work publishes in permitted test area; re-open shows exact text once |
| FB-04 | Incoming Messenger | A willing test person's message appears and Work can read it |
| FB-05 | Outgoing Messenger | Work replies in same existing conversation; person receives it |
| FB-06 | Event UI | Work can view/create an event draft and list required fields |
| FB-07 | Context persistence | Second browser run finds prior post and message thread |
| FB-08 | Duplicate prevention | Re-run does not publish/reply twice |
| FB-09 | Failure handling | Blocked message/login/post yields explicit report, no false success |
| FB-10 | Privacy | No identifying member records/screenshots committed to GitHub |

## Dry-run flow (no real participants required)
1. Use test FB group or approved limited area; test post: "TEST – Exkursion Biobauernhof: Wer möchte führen?"
2. Test member volunteers by comment or Messenger.
3. Work asks an initial guide question; a second message answers it; Work asks a follow-up only for missing info.
4. Prepare event draft for 3 seats. **Do not actually invite real users** unless authorized.
5. Simulate five reservations in an internal exercise: first 3 explicitly confirmed, numbers 4/5 waitlisted, one cancellation promotes number 4 and leaves number 5 waitlisted.
6. Confirm Work recognizes that clicking Facebook "Interested" is not a reservation.
7. Check one reminder route without sending unsolicited messages.

## Result report template
- Date:
- Browser actions actually attempted:
- FB-01 … FB-10: PASS / FAIL / NOT TESTED, with brief reason:
- Facebook URL(s) of **public/test posts only** (avoid private messenger and private event URLs in public reports):
- Approvals or manual handovers:
- Estimated Work usage, if visible:
- Go/no-go for recurring operation:
