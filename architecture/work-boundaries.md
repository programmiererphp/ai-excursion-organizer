# Architecture and real-world limitations

**Artifact ID:** EXK-ARCH-01

## External experience
Facebook Group = discovery and membership
Facebook group event = schedule, program, questions, signup thread
Messenger = private interview with guides and participant clarification
Facebook page (where supported) = public-facing admin identity

No email / external event registration / website / third-party participant portal.

## Execution
ChatGPT Work uses its **Cloud Browser** to open authenticated Facebook/Messenger pages and perform actions. No Groups API or unofficial scraping automation is assumed. This repository contains **Work instructions** and acceptance tests, not a browser agent executable independently of ChatGPT.

Cloud Browser is supported on eligible paid ChatGPT plans, but each website may restrict access, logins may expire, and consequential actions may require user confirmation. It is not guaranteed to operate Facebook/Messenger or be able to initiate unsolicited messages.

Work tasks may be scheduled, but Facebook Messenger incoming messages are **not** listed as a supported event-trigger source in ChatGPT Scheduled Tasks documentation (checked 2026-10-08). Use periodic inbox checks, not promises of immediate replies. Plus has a limited number of active scheduled tasks and Work usage limits.

## Persistence and privacy
**Canonical participant data:** Facebook event discussion, replies, Messenger threads; never a public GitHub data file.
**Canonical guide discussion:** existing Messenger thread.
**Repository:** public documentation, prompts, manual tests, anonymized metrics only.
**Optional:** store public Facebook group/event links (only public URLs) in a markdown index once available.
Never store individual names, private event links, screenshots of private conversations, session cookies, sign-in tokens, or password material in this repository.

## Main operating risks & mitigations
- Browser/UI changes: use observable state, no hard-coded selectors; report when blocked.
- Facebook messages unavailable / page identity restrictions: verify in pilot; do not silently reroute to Gmail.
- Moderation is periodic, not instantaneous: explicit operating hours in group description.
- Inconsistent attendance: always re-read prior confirmations; first-confirmed order and waitlist.
- Work plan limits: use only one initial pilot run. Later try one daily task and one weekly task; monitor actual usage.
- Formal bookings, payments, identity checks, public organizer approval: pause for human authorization when needed.

## External references
- [OpenAI Cloud Browser](https://help.openai.com/en/articles/20001280-using-cloud-browser-in-chatgpt)
- [OpenAI Scheduled Tasks](https://help.openai.com/en/articles/10291617-scheduled-tasks-in-chatgpt)
- [Facebook Group events](https://www.facebook.com/help/185716894811068/)
