# Broken TryHackMe rooms

A dated record of reported problems in TryHackMe rooms. Entries describe the reported problem without flags, answers, or walkthroughs. The reports below come from a summary of sent emails supplied by the repository owner; they have not been independently rechecked.

## Rooms

| Room | First email report | Reported problem |
| --- | --- | --- |
| [sustah](https://tryhackme.com/room/sustah) | 2026-07-20 | No machine available to boot. |
| [SafeZone](https://tryhackme.com/room/safezone) | 2026-08-01 | PHP commands ran under the wrong execution context, blocking the intended privilege escalation step. Follow-up emails were sent on 2026-08-30 and 2026-09-16. |
| [Metamorphosis](https://tryhackme.com/room/metamorphosis) | 2026-08-15 | The admin form returned an empty HTTP 500 response on a fresh instance. A follow-up email was sent on 2026-09-16. |
| [NoNameCTF](https://tryhackme.com/room/nonamectf) | 2026-08-31 | All 65,535 TCP ports appeared filtered; a packet capture showed outgoing probes without replies. A follow-up email was sent on 2026-09-16. |
| [biteme](https://tryhackme.com/room/biteme) | 2026-09-16 | Mentioned in a follow-up about previously reported rooms; the supplied summary contains no technical details or earlier report date. |
| [Looking Glass](https://tryhackme.com/room/lookingglass) | 2026-09-20 | Hostname changes and restricted directory permissions appeared to disrupt the intended enumeration path after an upgrade. |
| [forbusinessreasons](https://tryhackme.com/room/forbusinessreasons) | 2026-10-19 | The target was unreachable and all TCP ports appeared filtered. Restarting the lab and AttackBox did not restore access. |

These are dates of emails, not confirmed dates when the problems began. The current state of each room is unknown.

## Add or update a room

Add a row to [`rooms.csv`](rooms.csv) with:

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

The CSV is the source of truth. Update it through a pull request or a direct edit on GitHub.
