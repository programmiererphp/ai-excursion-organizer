# Facebook browser feasibility pilot — 2026-10-08

Artifact ID: EXK-PILOT-20261008-01
Status: PARTIAL — interface checks passed; end-to-end publication and messaging NOT TESTED.
Recurring operation: NO-GO until the remaining tests pass and the user separately authorizes scheduling.

## Scope and evidence
Read README, concept/vision-v1.md, concept/facebook-only-workflow-v2.md, architecture/work-boundaries.md, architecture/decision-rules.md, prompts/work-01-setup-and-pilot.md and tests/pilot-acceptance.md.
Observed actual Facebook UI in Cloud Browser. An authenticated session already existed; secure login handoff was unnecessary.

Only anonymized notes are recorded here. No private conversation text, person names, account IDs, private URLs, screenshots, cookies or credentials are included.

## Results
| Check | Result | Observed evidence / remaining gap |
|---|---|---|
| Facebook login | PASS | Authenticated Facebook loaded. |
| Page/group admin capability | PASS for existing Page | Switched to an existing Page, opened its group-creation form showing the Page as administrator, and accessed admin tools for an existing group. The new excursion identity/group has not been created or tested. |
| Group post | NOT TESTED end-to-end | Composer opened in the existing Page identity. Audience explicitly public; left empty and closed. No approved private test area was identified. |
| Event creation interface | PASS, interface only | Opened group-event form under Page identity; inspected title, start date/time, timezone, optional end, in-person/online, location, group audience, description and optional category/co-host/ticket/repeat controls. No event was published or saved. |
| Incoming Messenger | PARTIAL | Page Messenger link opened Meta Business Suite with historical incoming messages visible. No new controlled test message received. |
| Outgoing Messenger | NOT TESTED | Reply editor visible; no willing test recipient designated, no text entered or sent, no delivery verified. |
| Session continuity | PARTIAL | Page-admin group remained accessible after reload and identity switching. Cross-run recovery of a newly created test post/thread remains untested. |
| Notification/inbox access | PASS | Page notification panel and Page Messenger inbox opened successfully. |

Table ID: EXK-PILOT-MATRIX-20261008-01

## Actions and limits
- Checked personal-profile managed groups and the available Page identities; no intended excursion group was identified in the inspected views. This was not an exhaustive search across every Page.
- An existing unrelated Page/group was used solely to inspect capabilities, not repurposed.
- Group-post composer was closed empty.
- Event form was discarded after inspecting in-person mode.
- Reload verified authenticated group admin access.
- Restored original personal-profile identity and verified it.
- Opening inbox/notification interfaces may affect read indicators.
- No new Page or group, post, event, invitation, message or recurring task was created.
- No site-served technical block was observed during these checks; outstanding items are testing/authorization gaps, not proven Facebook feature failures.

## Important creation default
The Page-owned group-creation form had its "invite followers" switch ON by default. Turn this OFF and verify before submitting any approved test or production group creation. The inspected event form's "invite all group members" switch was OFF.

## Acceptance mapping
- FB-01: PASS.
- FB-02: PARTIAL against the intended excursion identity; existing-Page capability confirmed.
- FB-03: NOT TESTED.
- FB-04: NOT TESTED for a new willing test person's message; historical inbound visibility confirmed.
- FB-05: NOT TESTED.
- FB-06: PASS for creation interface and field inspection only.
- FB-07: PARTIAL; same-run reload passed, post/thread retrieval in a second run pending.
- FB-08: NOT TESTED with a created test artifact; no publishing or sending retries occurred.
- FB-09: Reporting distinguishes observed UI from execution; no failed send/login/post was induced.
- FB-10: PASS for this report.

## Proposed public community — DRAFT, NOT APPROVED
Name: Exkursionen & Entdeckungen Göttingen

Two-sentence description:
Gemeinsam entdecken wir Göttingen und Umgebung – von Natur und Geschichte bis zu Höfen, Werkstätten und besonderen Orten. Mitglieder schlagen Ziele vor oder übernehmen die Leitung einzelner Ausflüge; Planung, Anmeldung und Rückfragen bleiben vollständig hier auf Facebook.

Category/theme: Freizeit, Ausflüge und lokale Gemeinschaft. This is a proposed theme, not a verified selectable Facebook category. The inspected group-creation form had no category field.

Simple rules:
1. Freundlich bleiben; Beiträge beziehen sich auf gemeinsame Entdeckungen in Göttingen und Umgebung.
2. Jede Exkursion braucht eine benannte Leitung sowie klare Angaben zu Treffpunkt, Dauer und Kosten.
3. Ein Platz ist erst nach ausdrücklicher Bestätigung reserviert; „Interessiert“ oder „Zusagen“ allein genügt nicht.
4. Absagen zeitnah mitteilen; keine Werbung, ungefragten Einladungen oder Veröffentlichung privater Nachrichten.

## Proposed continuation — awaiting user decision
1. Approve either a dedicated public excursion Page with the proposed name or explicitly select an existing Page for the pilot.
2. Approve a private, hidden group named "TEST – Exkursionen & Entdeckungen Göttingen", with follower invitations disabled and no invitations to real people.
3. Publish exactly one marked TEST post there, reopen it, and verify exact text and absence of duplicates.
4. The user may act as the willing tester by initiating a TEST Messenger message to the selected Page. Verify the incoming message, send one authorized test reply, reopen it, and obtain receipt confirmation.
5. In a later run, retrieve both artifacts without duplication.
6. Only after pilot completion and separate approval, create the proposed public community. Then prepare one short local excursion with one confirmed human guide; publish an event only after details and permission are settled.

## Continuation — 2026-10-08, after setup approval
The user selected a new dedicated excursion Page, agreed to act as the Messenger tester, and approved the proposed setup. The browser session remained authenticated in this later turn. Page creation was opened and Public Page selected. Before the details form, Facebook displayed a notice that clicking Get started accepts Facebook Page Terms. The action was not submitted: browser policy requires explicit confirmation at this contractual acceptance step. Waiting for that specific confirmation. No Page, group, post, invitation, message or recurring task has been created in this continuation. The confirmation screenshot is kept outside public GitHub; no personal browser data has been committed.
