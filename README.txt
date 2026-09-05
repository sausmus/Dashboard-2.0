Teacher Dashboard 2.0 — Bell + New School Year Reset Update

Replace these files in the Dashboard 2.0 GitHub repository:

ROOT
- index.html
- bell-countdown.html
- settings.html

SHARED FOLDER
- shared/dashboard-data.js
- shared/bell-service.js

No other utility HTML files need to be replaced for this update. Agenda, Student Picker,
Participation Tracker, and Scoreboard already load shared/bell-service.js, so their mini bell
controls pick up the new behavior automatically.

WHAT CHANGED
1. Main Dashboard bell control is now a compact upper-right pill on larger screens.
2. Bell Countdown is disabled on Saturday and Sunday and displays "No School Today."
3. Custom warning buttons turn green with a check mark when armed in both the full Bell Countdown
   and all mini bell controls.
4. Dashboard Settings now explains "Current Class Across Apps" more clearly.
5. New School Year Reset wording now clearly separates what WILL reset from what WILL NOT change.
6. New School Year Reset now backs up and clears Scoreboard championship/results data.
7. The reset also clears Student Picker pools/history/groups and Participation Tracker undo history,
   while preserving Student Picker preference choices.
8. Undo Last School Year Reset restores the complete pre-reset state across Dashboard data,
   Scoreboard, Student Picker, Participation Tracker, and bell-session state.
9. Bell schedules, alarm sound preferences, Final Bell setting, custom warning default, and Agenda
   history are not changed by a New School Year Reset.

TESTS RUN
- JavaScript syntax validation passed.
- New School Year Reset + Undo restoration test passed.
- Saturday/weekend Bell Countdown test passed.
