# Changelog

## 1.0.0 — Initial public release

- Initial public release of Financial Aid Office Workflow as a standalone plugin repository.
- Added the `financial-aid-office` plugin with the `financial-aid-operations` skill covering case review, missing-document follow-up, verification and conflicting-information preparation, appeal and professional-judgment preparation, loan workflow, reconciliation and closeout preparation, and office reviews.
- Includes a source hierarchy, data-minimization rules, and stricter regulated-decision boundaries: no final eligibility determinations, aid adjustments, certifications, or money movement without institutional authority.
- Includes escalation rules for missing sources, conflicting sources, uncovered exceptions, and unverifiable deadlines.
- Added a GitHub Actions workflow that validates the manifest, semantic version, skill frontmatter, and required documentation.

### Verification

Package validation runs in GitHub Actions. This release has not been installed or exercised in a user's Claude runtime by its authors; smoke-test the plugin in your own Claude environment after installing it.
