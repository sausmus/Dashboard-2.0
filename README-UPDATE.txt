Teacher Dashboard — Shared Bell Integration Update

Replace these existing root files:
- index.html
- agenda.html
- bell-countdown.html
- student-picker.html
- participation-tracker.html
- scoreboard.html
- settings.html

Replace this shared file:
- shared/dashboard-data.js

ADD this new shared file:
- shared/bell-service.js

Keep bjh-logo.png in the root directory (included here for convenience).

WHAT CHANGED
1. Bell schedules now live in shared/dashboard-data.js.
2. Minimum-day dates can be added from Dashboard Settings.
3. Automatic schedule priority:
   - Saved minimum-day date -> Minimum Day
   - Otherwise Wednesday -> Late Start
   - Otherwise -> Regular
   Manual schedule selection remains available.
4. Bell Countdown intentionally ignores hidden-period settings and always uses
   the complete school bell schedule, including Snack and Lunch.
5. Every dashboard utility now has the same mini Bell Countdown dropdown.
6. Warning alarms are shared in localStorage. Arm a warning in one utility and
   it remains armed when you navigate to another utility.
7. Any key press or pointer click stops an active warning alarm.
8. Settings now has a New School Year Reset:
   Clears rosters, hidden periods, custom period names, minimum-day dates,
   and participation records.
   Keeps bell schedules, Scoreboard history, and app preferences.
   A one-reset backup is created for Undo Last School Year Reset.

IMPORTANT
All files must be served from the same GitHub Pages site/origin so localStorage
can be shared across utilities.
