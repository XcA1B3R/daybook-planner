# Daybook Planner: release process

The owner wants every release kept. For each new version:

1. Bump the version (minor changes: v1.1, v1.2; big changes: v2.0).
2. Make the change in `index.html` (the site root always serves the latest version).
3. Copy the new `index.html` to `versions/<version>/index.html`. Never edit or delete older folders under `versions/`.
4. Add the version to the list in `versions/index.html` (newest first, under "Latest").
5. Add an entry at the top of `CHANGELOG.md` saying what changed in plain language.
6. Commit and push to `main`. (Tag the release too if tag pushes are allowed; the `versions/` folder is the archive either way.)

The planner is a single self-contained `index.html`. Saved entries live in the browser's localStorage under the key `daybook-v1`, which all versions share, so never rename that key without a migration.

Testing: the page exposes a read-only `window.__daybook` hook (`blocksOn(date)`, `goDay(date)`) for automated browser tests. Keep it read-only.

Privacy: Strava keys and tokens live in localStorage under `daybook-strava`, and the Google token under `daybook-gtoken`. Never write either into the repo.

Beta: `beta/index.html` is the v3.0 test build (Firebase sign-in with Google plus a TOTP authenticator code, Firestore sync). It uses its own storage keys (`daybook-v3-cache`, `daybook-v3-strava`, `daybook-v3-gtoken`) and only reads `daybook-v1`/`daybook-strava` for a one-time import, so the main version is never affected. Don't promote it to the root until the owner approves; then archive it as `versions/v3.0/` like any release.
