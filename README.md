# Broken TryHackMe rooms

A dated record of TryHackMe rooms that appear to be broken. Entries should describe an observed problem, not contain flags, answers, or walkthroughs.

## Rooms

No rooms have been recorded yet.

## Add or update a room

Add a row to [`rooms.csv`](rooms.csv) with:

- The room name and URL.
- `date_found`: the date you first observed the issue, in `YYYY-MM-DD` format. If the exact date is unknown, leave it blank and explain that in `notes`.
- A short description of what failed and how to reproduce it without revealing challenge answers.
- An evidence link when available, such as a screenshot or a public issue report. Do not publish private account details or flags.
- A status of `broken`, `intermittent`, or `fixed`. When a room is fixed, keep its original `date_found` and add `date_last_checked`.

Only list problems you have directly observed or can verify from evidence. Dates are observation dates, not claims about when a room first became broken.

## CSV columns

| Column | Meaning |
| --- | --- |
| `room_name` | Display name of the room |
| `room_url` | Link to the room |
| `date_found` | First observed broken date (`YYYY-MM-DD`) |
| `issue` | Brief description of the failure |
| `evidence_url` | Optional link supporting the report |
| `status` | `broken`, `intermittent`, or `fixed` |
| `date_last_checked` | Most recent verification date (`YYYY-MM-DD`) |
| `notes` | Additional context, including uncertain dates |

The CSV is the source of truth. Update it through a pull request or a direct edit on GitHub.
