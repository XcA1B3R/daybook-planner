# Changelog

Each version is kept at `versions/<version>/` and tagged in git. The site root always serves the latest version.

## v1.5 · 2026-10-24

- Google Calendar now works on the GitHub site, not just inside Claude. The planner signs in to Google directly, and only reads your calendar.
  - One-time setup: create a free Google sign-in ID (OAuth client ID) and paste it into Customize › Google Calendar. Step-by-step instructions are built in.
  - Events refresh every 5 minutes while the planner is open, and when you come back to it.
  - Google sign-ins last an hour. After that, the planner keeps showing your last-known calendar and offers an **Update calendar** button.
- Inside Claude, Google Calendar still connects through Claude, as before.

## v1.4 · 2026-10-24

- The Day schedule is now a time grid. Each block is drawn at its actual start and end times, with a red line marking the current time.
- New activity blocks: Work, Gym, Swim, Sauna, Walk and Ride.
  - Drag one onto the schedule, or tap one and then tap a time.
  - Drag a block to move it, and drag its top or bottom edge to change the start or end time. Everything snaps to 15 minutes.
  - Tap a block to change the activity, start, length or note, copy it to tomorrow, or remove it.
- Google Calendar events show in the same grid, side by side with your blocks when they overlap.
- Blocks also appear on the Week and Family pages and in the Home "Up next" card.

## v1.3 · 2026-10-23

- Weeks now start on Sunday on every page: year, month, week, family, habit tracker and the workout charts.
- Week and family entries saved under the old Monday-start weeks move automatically to the matching days.
- New **Customize › Reset planner** erases all entries. You confirm by typing RESET, and you can choose to keep your theme, cover, logo, title and Google Calendar connection.
- The Home greeting now uses the name from a title like "Dean's Daybook" ("Good morning, Dean").

## v1.2 · 2026-10-23

- Upload your own logo in Customize › Logo (PNG, JPG, SVG or WebP). It's resized automatically and appears in the top left, on the cover and as the browser tab icon. "Use the default logo" switches back.
- Customize › Title sets the planner's title. It shows next to the logo, on the cover and in the Home greeting.
- Fixed: closing the Customize menu now returns focus to the Customize button.

## v1.1 · 2026-10-23

- Replaced the "Daybook" wordmark in the top left with a notebook logo. It takes on the colors of your light or dark style, and tapping it opens the cover.

## v1.0 · 2026-10-23

First GitHub release.

- Ring-bound planner design with divider tabs, month tabs, a cover page, stickers, and light and dark styles
- Home dashboard: up next, today, year progress, family, coming up, goals, habits, budget, debt payoff, workouts and work notes
- Year, Month, Week and Day pages with US holidays and an hourly schedule
- Goals & Habits, Budget, Fitness, Family (activities, meal plan, grocery list) and Work Notes
- Phone layout with a bottom tab bar, swipe between dates, quick add, and moving to-dos to tomorrow
- Google Calendar works only inside Claude; outside Claude, entries stay on the device
