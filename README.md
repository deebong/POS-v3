# POS v3 — Production Repository

**README version:** 3.0.0  
**Product version:** 3.0.0  
**Status:** PRODUCTION — designated production repository. This label identifies the repository's role; it does not imply that a release has been deployed or validated.

## Repository roles
- `deebong/POS-platform-v3` — private source of truth, tests, Apps Script, and controlled deployment workflows.
- `deebong/POS-v3-staging` — public staging build for testing and acceptance only.
- `deebong/POS-v3` — public production repository and production-release target.
- v2 repositories — historical/stable reference; do not modify from v3 work.

## Version policy
- Initial production track: `3.0.0`.
- `VERSION` in the private source repository is the canonical project version.
- The application version and Apps Script `POS_VERSION` marker must match the release version.
- Staging and production metadata must identify the exact source commit and build version.
- Do not call the app production-ready until source migration is complete, required checks pass, and the exact validated build is deliberately promoted.

## Release flow
1. Implement and test changes in `POS-platform-v3`.
2. Publish a versioned build to `POS-v3-staging` for validation.
3. Promote only the exact validated build to this repository after explicit approval.
4. Preserve the prior production release for rollback.

## Current release status
- Repository role: production target.
- Intended product version: `3.0.0`.
- Source migration, CI validation, and staging verification are not yet confirmed complete.
- No production promotion has been performed by this README initialization.
