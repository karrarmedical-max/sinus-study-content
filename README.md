# Sinus Study · Content

The live content file for the **Sinus Study** app by NovaMed.

The app downloads `content.json` whenever the phone is online, so changes here reach every student without sending a new APK:
subjects and their importance, daily minutes per level, "how to read" guides, the official exam timetable, announcements, and the developer card.

## Rules for every update

- Raise `version` by 1. The app only accepts a file whose `version` is higher than the one it already has.
- Set `updated` to today's date (`YYYY-MM-DD`).
- Exams go in `exams` as `{ "id": "unique", "s": "<subject id>", "type": "final", "date": "2027-01-10", "time": "09:00", "place": "" }`.
  Types: `daily`, `quiz`, `lab`, `seminar`, `midterm`, `final`, `practical`, `other`.
- Announcements go in `news` as `{ "id": "unique", "date": "2026-10-22", "text": "..." }`. The newest one shows on the home screen.
- To tell students a new APK exists, set `latestApp` to its version (for example `2.3.0`); the app shows a download banner linking to `appLink`.

No student data is ever stored here.
