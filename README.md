# AI Excursion Organizer

**Status: Delivery 1 – Facebook-only Work pilot (not live yet)**

A decentralized excursion community: AI researches destinations, invites people to lead excursions, helps prepare visits and travel, and coordinates participants. **All participant- and guide-facing conversations happen solely on Facebook (group posts, Facebook Events, comments and Messenger).** No email, Luma, external sign-up site, or standalone webapp.

ChatGPT **Work + Cloud Browser** is the intended operator. This repository stores versioned concepts, instructions, templates, and test artifacts; it is **not the public registration channel** and it is **not an already running Facebook bot**.

## Start here

1. [Concept / vision](concept/vision-v1.md)
2. [Facebook-only end-to-end workflow](concept/facebook-only-workflow-v2.md)
3. [Work architecture and operational limits](architecture/work-boundaries.md)
4. [Delivery 1 setup and browser pilot prompt](prompts/work-01-setup-and-pilot.md)
5. [Pilot acceptance tests](tests/pilot-acceptance.md)
6. [Delivery roadmap](deliveries/delivery-01.md)

After the browser pilot passes:
- [Daily Facebook inbox & moderation prompt](prompts/work-02-inbox-and-moderation.md)
- [Weekly excursion research prompt](prompts/work-03-destination-research.md)
- [Guide interview](templates/guide-dialog.md)
- [Event announcement](templates/event-post.md)
- [Operational rules](architecture/decision-rules.md)

## Principles

- **One platform externally:** Facebook/Messenger only for participants and guides.
- **Distributed leadership:** an excursion runs only when a suitable human guide takes responsibility for conducting it.
- **Work assists:** planning, questions, moderation, event announcements, reservation tracking and reminders as permitted by Facebook.
- **Confirm, don't assume:** RSVP 'Interested'/'Going' is not a confirmed place unless admin explicitly confirms.
- **Privacy:** this is a **public GitHub repository**. Never commit participant names, Messenger transcripts, personal identifiers, phone numbers, private Facebook screenshots, cookies or credentials.
- **No fabricated execution:** distinguish templates, drafts, browser-tested actions and actually published Facebook content.
- **Incremental:** test Facebook browser access and Messenger first; do not activate unattended automations before tests.

## Implementation stage

The Work prompts are ready to run. **Facebook group creation, login and live messages have not been performed by this repository commit.** Launch a Work task with the setup prompt, authorize Facebook securely when asked, then record only non-personal test outcomes under `tests/`.

## Source references (checked 2026-10-08)

- [ChatGPT Cloud Browser](https://help.openai.com/en/articles/20001280-using-cloud-browser-in-chatgpt)
- [Scheduled Tasks](https://help.openai.com/en/articles/10291617-scheduled-tasks-in-chatgpt)
- [Facebook: create a group event](https://www.facebook.com/help/185716894811068/)
