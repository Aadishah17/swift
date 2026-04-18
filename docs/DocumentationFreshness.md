# Documentation Freshness

This document defines ownership and review cadence for high-impact contributor
guides so they stay accurate as workflows evolve.

## Scope

The following guides are considered "freshness critical":

- `/docs/HowToGuides/GettingStarted.md`
- `/docs/Testing.md`
- `/docs/ContinuousIntegration.md`
- `/docs/HowToGuides/ContributorQuickstart.md`

## Ownership model

- **Primary owner**: the author of a PR that changes related workflows.
- **Review owner**: the code owner automatically requested by CODEOWNERS.
- **Escalation owner**: maintainers in the `@swiftlang/swift-branch-managers`
  group when broad project policy changes are required.

## Cadence

- Review freshness-critical docs at least **once per quarter**.
- During each review, verify:
  - Referenced commands still exist.
  - Links and anchors still resolve.
  - CI guidance still matches current bot/workflow behavior.
  - "First-day" recommendations still reflect the fastest onboarding path.

## Update criteria

Update these docs whenever any of the following changes land:

- Build/test entry points or required flags.
- CI trigger phrases, labels, or test defaults.
- Contributor workflow changes (review process, ownership, branch policy).
