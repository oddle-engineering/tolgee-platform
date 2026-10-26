# Oddle Tolgee fork

This repository is an Oddle-maintained fork of [Tolgee Platform](https://github.com/tolgee/tolgee-platform).

- Production baseline: `v3.240.2`
- Oddle overlay branch: `oddle/v3.240.2+oddle`
- First custom setting: `tolgee.rate-limits.user-limits`

Set `user-limits: false` to disable the authenticated-user global bucket while
keeping the global IP, endpoint, and authentication buckets enabled.

The `upstream` Git remote tracks the Tolgee repository. This fork is intended
for Oddle-specific Tolgee changes generally; each feature should remain a
small, reviewable overlay commit. When upgrading, start from the desired
upstream release tag, replay the Oddle overlay commits, run the tests, and
publish a new pinned container image. Do not build or deploy on the production
Tolgee host.
