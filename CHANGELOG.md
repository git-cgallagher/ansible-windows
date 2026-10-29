# Changelog

Notable changes to this repository. Earlier history is in the git log.

## 2026-10-29

- Added `SECURITY.md`: report security problems privately through GitHub's advisory form
  (private vulnerability reporting is now on).
- `main` is now protected by the repo ruleset "main protection" (id `26118895`). Changes land
  only through pull requests (0 approvals; there is no CI, so no required checks), and
  force-pushes and deleting `main` are blocked. Also turned on secret scanning, push protection,
  Dependabot alerts and security updates, and delete-branch-on-merge.
