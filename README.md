# Broken TryHackMe rooms

Broken rooms waste learners' time. This repository tracks reported TryHackMe room failures, when they were reported, and when someone last checked them.

## Why this exists

It is ridiculous for a broken room to stay live without a warning after the problem has been reported. Learners can waste hours debugging a dead machine or a broken intended path, wondering whether they missed something when the lab itself is at fault. They should not have to search Discord or scattered online posts to find out whether a room works. TryHackMe should mark known problems clearly, fix or temporarily withdraw affected rooms, and tell reporters when a fix is confirmed.

I started this tracker because I reported rooms that appeared broken and could not see a reliable public record of their status or learn when they were fixed. Community discussions on Discord and elsewhere suggest that some problems may have persisted for more than a year. Those longer-running claims need dated, linked evidence before they are presented here as verified cases.

The goal is accountability and useful information for learners: what failed, when it was reported, whether it still fails, and when it was last checked. Entries describe the problem without flags, answers, or walkthroughs. The reports below come from a summary of sent emails supplied by the repository owner; they have not been independently rechecked.

## Why leave a known broken room available?

If a room has been confirmed broken and is waiting in a fix backlog, what is the reason for keeping it accessible without a warning? Learners deserve an explanation. A backlog is not a good reason to keep an unusable room playable, and a larger room count is no benefit if learners cannot trust the catalog. This tracker does not claim to know TryHackMe's motives or internal process, but the likely costs are easy to see:

- **Learners lose time.** Someone may spend hours repeating steps, restarting machines, or debugging an unsolvable path. The frustration is worse when the platform already knows about the problem.
- **Compute can be wasted.** Learners may keep broken machines and AttackBoxes running, or try resource-intensive approaches against a path that cannot work. The size of that cost is unknown, but it is avoidable.
- **Trust in working rooms suffers.** Once you have encountered broken rooms, every difficult but valid challenge starts to look suspect. Learners may turn to walkthroughs just to find out whether the room works, spoiling a challenge that was actually fine.
- **Support gets repeat reports.** If a known issue has no visible status, more learners may spend time reporting the same failure, and support may spend time answering them individually.
- **Support staff bear the frustration.** They may have to deliver the same disappointing answer to people who have already lost time. This is a concern about the experience, not a claim about staff morale or internal workload.
- **Progress becomes harder to trust.** A failure caused by the lab can feel like a failure to learn. That can discourage learners and make completion statistics less meaningful.

## A straightforward response

Temporarily disable access to a room once its issue is confirmed and it enters the fix backlog. Keep a visible status notice and the issue report available so learners know why it is unavailable. Reopen the room after the affected path has been tested, record the fix date, and notify people who reported the problem. If a room can remain partly usable, say exactly what is broken before someone starts it.

## Rooms

| Room | First email report | Last checked | Reported problem |
| --- | --- | --- | --- |
| [sustah](https://tryhackme.com/room/sustah) | 2026-07-20 | Not checked | No machine available to boot. |
| [SafeZone](https://tryhackme.com/room/safezone) | 2026-08-01 | Not checked | PHP commands ran under the wrong execution context, blocking the intended privilege escalation step. Follow-up emails were sent on 2026-08-30 and 2026-09-16. |
| [Metamorphosis](https://tryhackme.com/room/metamorphosis) | 2026-08-15 | Not checked | The admin form returned an empty HTTP 500 response on a fresh instance. A follow-up email was sent on 2026-09-16. |
| [NoNameCTF](https://tryhackme.com/room/nonamectf) | 2026-08-31 | Not checked | All 65,535 TCP ports appeared filtered; a packet capture showed outgoing probes without replies. A follow-up email was sent on 2026-09-16. |
| [biteme](https://tryhackme.com/room/biteme) | 2026-09-16 | Not checked | Mentioned in a follow-up about previously reported rooms; the supplied summary contains no technical details or earlier report date. |
| [Looking Glass](https://tryhackme.com/room/lookingglass) | 2026-09-20 | Not checked | Hostname changes and restricted directory permissions appeared to disrupt the intended enumeration path after an upgrade. |
| [forbusinessreasons](https://tryhackme.com/room/forbusinessreasons) | 2026-10-19 | Not checked | The target was unreachable and all TCP ports appeared filtered. Restarting the lab and AttackBox did not restore access. |

These are dates of emails, not confirmed dates when the problems began. The current state of each room is unknown.

## Submit a room

Found a room that appears broken? [Open a room report](https://github.com/helpitisbroken/tryhackme-broken-rooms/issues/new?template=broken-room.md). You need a GitHub account to submit an issue.

1. Check the table above and [existing issues](https://github.com/helpitisbroken/tryhackme-broken-rooms/issues) for the same room and problem. If it is already listed, add your new observation to that issue instead of opening a duplicate.
2. Include the room name and URL, the date you first observed the problem, and the date you last checked it. Use `YYYY-MM-DD`; say `unknown` rather than guessing a date.
3. Describe what failed, what you expected, and the shortest safe steps that reproduce it. Mention whether restarting the room or AttackBox changed the result.
4. Add evidence you collected yourself, such as a redacted screenshot, error message, or relevant log excerpt. A report to TryHackMe support is helpful but not required. If you reported it, include the date; do not paste a private email thread.

Do not post flags, challenge answers, walkthroughs, credentials, personal details, or other users' private information. A report records an observed problem; it does not establish that the room is still broken today. If you later confirm a fix, update the issue with the date and what you tested.

You can also propose a change directly through a pull request. Add or update a row in [`rooms.csv`](rooms.csv) with:

- The room name and URL.
- `date_found`: the date you first observed the issue, in `YYYY-MM-DD` format. Leave it blank if unknown.
- `date_reported`: the date of the first email report in the supplied evidence, in `YYYY-MM-DD` format.
- A short description of what failed and how to reproduce it without revealing challenge answers.
- An evidence link when available, such as a screenshot or a public issue report. An email subject can identify a private report without publishing the email. Do not publish private account details or flags.
- A status of `reported`, `intermittent`, or `fixed`. Use `reported` when the current state has not been checked. When a room is fixed, keep its original dates and add `date_last_checked`.

Only list problems you have directly observed or can verify from evidence. Dates are observation dates, not claims about when a room first became broken.

## CSV columns

| Column | Meaning |
| --- | --- |
| `room_name` | Display name of the room |
| `room_url` | Link to the room |
| `date_found` | First observed broken date (`YYYY-MM-DD`), if known |
| `date_reported` | Date of the first email report supplied for this entry (`YYYY-MM-DD`) |
| `issue` | Brief description of the failure |
| `evidence_url` | Optional link supporting the report |
| `email_subject` | Subject of the first supplied email report |
| `status` | `reported`, `intermittent`, or `fixed` |
| `date_last_checked` | Most recent verification date (`YYYY-MM-DD`) |
| `notes` | Additional context, including uncertain dates |

The CSV is the source of truth. Accepted issue reports can be added to it after the supplied evidence is reviewed.
