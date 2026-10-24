# Daybook Planner: release process

The owner wants every release kept. For each new version:

1. Bump the version (minor changes: v1.1, v1.2; big changes: v2.0).
2. Make the change in `index.html` (the site root always serves the latest version).
3. Copy the new `index.html` to `versions/<version>/index.html`. Never edit or delete older folders under `versions/`.
4. Add the version to the list in `versions/index.html` (newest first, under "Latest").
5. Add an entry at the top of `CHANGELOG.md` saying what changed in plain language.
6. Commit, push to `main`, then tag: `git tag -a <version> -m "<version>"` and `git push origin <version>`.

The planner is a single self-contained `index.html`. Saved entries live in the browser's localStorage under the key `daybook-v1`, which all versions share, so never rename that key without a migration.
