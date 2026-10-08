# Facebook-only workflow (V2)

**Artifact ID:** EXK-FLOW-02
**Participants' single interface:** Facebook Group + Facebook Events + comments + Messenger.

## Lifecycle
1. **Research:** Work investigates a destination; checks accessible opening/visiting arrangements, group suitability, access, travel, likely costs, and source URLs. Unverified facts are marked.
2. **Candidate invitation:** Work drafts or posts a concise group proposal, with an explicit invitation for an excursion guide to comment or message the page/admin.
3. **Guide interview:** One-on-one Messenger dialog asks about familiarity with destination, realistic date/time, group size, program, trip duration, transport, access/venue booking, prices, weather alternative, donations and responsibilities.
4. **Verification:** Confirm any operator permission/booking with evidence from guide. A human reviews major commitments and selects the guide. Do not characterize the applicant as "verified" without real verification.
5. **Event publication:** Facebook group event with real date/time, meeting point, guide (only details the guide wants shown), complete costs and a clear reservation instruction.
6. **Registration:** One public event thread for "Anmeldung" comments; admin gives explicit confirmation in chronological order up to the stated capacity. Messenger may handle private questions or confidential details. "Going" / "Interested" alone does not reserve a place.
7. **Waitlist and changes:** After capacity, assign waitlist positions. On cancellation, offer place to next person; only then update official count. Work confirms with timestamps visible in Facebook conversation.
8. **Reminders:** Work messages registered participants through existing eligible Messenger threads; where a direct message is unavailable, use the event discussion post/notification mechanism. Never claim a message was delivered without checking.
9. **Event execution:** The human guide runs the outing and manages any in-person safety/venue requirements.
10. **Follow-up:** Facebook event comment requesting optional feedback. Prepare next ideas; summarize results without exposing personal data in public GitHub.

## Guide statuses
`candidate -> interviewing -> pending-arrangements -> pending-approval -> approved -> event-published -> completed`
Alternative: `on-hold / declined / cancelled`.

## Excursion statuses
`idea -> looking-for-guide -> preparing -> ready-for-approval -> published -> completed`
Alternative: `postponed / cancelled`.

## Example signup state (only inside Facebook)
- Capacity 12; 10 confirmed, 2 places open, 3 waitlisted.
- RSVP 'Interested' without comment: not counted.
- Members registering multiple times: one person, one place.
- Leader/organizer only counts if explicitly registered as a participant.
- Work must inspect existing confirmations before each new update (no double-booking).

## Operational consistency
- Avoid overlapping Work runs. Finish pending inbox checks before the next.
- Work should link to the corresponding Facebook event in its own run report and keep the report free of Messenger quotations and personal details.
- When the UI offers no sufficiently clear participant order or counter, pause automation of confirmations and request review.
- For each event publish a prominent single source of truth: event description + pinned/latest admin comment. Do not create new groups for each outing during pilot.
