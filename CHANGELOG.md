# Changelog

Each version is kept at `versions/<version>/` and tagged in git. The site root always serves the latest version.

## v2.1 · 2026-10-24

- **Google Calendar renews itself.** When the one-hour Google sign-in runs out, it renews the next time you tap anywhere in the planner. You may see a Google window flash for a moment, and there's no button to press. The last-known calendar stays on screen in the meantime. If Google can't renew automatically, an **Update calendar** button appears.
- **New Health page:**
  - A daily check-in for weight, sleep, steps, resting heart rate, blood pressure, water, energy (1–5) and notes. It saves as you type, and the arrows move between days.
  - Summary tiles: latest weight and its 30-day change, 7-day averages for sleep, steps and resting heart rate, and your latest blood pressure with its standard category (normal, elevated, stage 1, stage 2).
  - Charts: weight over 90 days, sleep and steps over 14 days, resting heart rate over 30 days, blood pressure ranges over 30 days, and water. Tap any point for details.
  - Lists for medications and supplements, and for appointments. Upcoming appointments also appear in Home's "Coming up".
  - Targets for weight, sleep, steps and water, shown as goal lines.
- A Health card on Home shows your latest weight, last night's sleep, today's steps and a 30-day weight line.
- Health data is entered by hand. Google's health data can't be read by a web page today.

## v3.0 beta · testing at /beta/ (not yet the main version)

- Sign in with Google, then a 6-digit code from an authenticator app such as Google Authenticator. The first sign-in walks you through adding Daybook to the app with a QR code or setup key.
- Your entries, settings, logo, Google Calendar sign-in ID and Strava connection are stored in your own Firebase account, so they follow you to every device you sign in on.
- On first sign-in, the beta copies the entries saved on that device by the main version. It only reads them and never changes or deletes them. **Customize › Account** can copy them again from any device.
- The beta keeps its own copy of your data on each device, separate from the main version, so the two never interfere.
- **Sign out of this device** clears the beta's local copy. Your account data stays safe in Firebase.

## v2.0 · 2026-10-24

- The Fitness page now opens with a dashboard:
  - **This week:** time, miles and workouts so far, compared with last week.
  - **Weekly goal:** a ring showing progress toward a weekly hours goal you set (5 hours to start), plus how many of the last 11 weeks you met it.
  - **Day streak:** your current run of days with a workout, and your best this year.
  - **Weekly average:** for the year and for the last 11 weeks.
  - **Hours per week:** a chart of the last 12 weeks with your goal line.
  - **Miles through the year:** a running total compared with last year at the same point, with how far ahead or behind you are.
  - **Activity calendar:** a square for every day, shaded by workout time. It opens scrolled to today.
- Tap or hover any bar, point or day for its numbers.
- The year summary and activity cards follow the dashboard, and the Strava panel now sits below them.
- Chart scales use finer steps, so a year with 2,000 miles tops out at 2,500 instead of 5,000.

## v1.9 · 2026-10-24

- Tap a workout on the Day grid or in the Fitness log to open a details card in the planner.
  - It shows distance, moving and elapsed time, average and max speed (or pace for runs, walks and hikes), climbing, heart rate, power, cadence, calories and kudos when available.
  - Strava workouts include a sketch of the route, and the card loads your Strava description, bike or shoes, and device.
  - **Open on Strava**, **Show on the day** and **Delete from log** are on the card. Delete asks you to tap twice.
- Strava imports now save those extra details. Tap **Re-check this year** once to add them to workouts already imported.

## v1.8 · 2026-10-24

- The Fitness page opens with a **year so far** summary for the selected year: total workouts, hours, miles, active days and climbing.
- Each activity type gets a card, with rides and walks first. A card shows the count, total time and miles, average per workout, longest effort with its date, climbing, and a month-by-month chart. Tap a bar for that month's numbers.
- Strava imports now save elevation gain. Tap **Re-check this year** once to add it to workouts already imported.

## v1.7 · 2026-10-24

- **Strava sync** on the GitHub site. Set it up in the Strava panel at the top of the Fitness page.
  - Create a free Strava API app and paste its Client ID and Secret. They're saved only in that browser, never in the repo.
  - Connect Strava and approve read-only access.
  - Activities from the start of the year import into the Fitness log: rides, runs, swims, walks, hikes, weight training and more, with time, miles and the activity name.
  - New activities sync automatically when you open the planner, at most every 30 minutes. **Sync now** and **Re-check this year** are on the panel.
  - Workouts never duplicate, and edits you make on Strava update the log.
- Completed Strava workouts show on the Day grid as orange ✓ tiles at the time you did them, next to your planned blocks. Tap one to open it on Strava.
- Imported entries in the Fitness log carry a Strava label that links to the activity.

## v1.6 · 2026-10-24

- Blocks can repeat: every day, on weekdays, every week on the same day, or on days you pick. You can also set an end date.
- Tap a repeating block and choose **This day only** or **Every repeat** before saving a change.
- Dragging or resizing a repeating block changes that day only. Use the editor to change every repeat.
- **Remove this day** skips one day. **Stop repeating from here** ends the series from that day on.
- Repeating blocks show a ↻ mark.
- The title of a tall block now sits below its top resize handle, so grabbing the title moves the block instead of resizing it.

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
