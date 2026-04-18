# CI and Test Health Tracking

This guide defines a lightweight process to track flaky tests and performance
signals, then prioritize stabilization work.

## Goals

- Keep pull request signal quality high.
- Reduce re-run churn caused by flaky tests.
- Surface regressions in test duration or failure rates early.

## Flaky test tracking

When a test is suspected flaky:

1. Open an issue using the `flaky test` template.
2. Add labels:
   - `area/tests`
   - a matching `area/*` label for the owning subsystem
3. Include:
   - Failing test path/name
   - Reproduction signal (CI links, frequency, platform)
   - Latest known good commit range, if known

## Performance trend tracking

- Use CI runtime summaries and workflow durations to monitor trend changes.
- File an issue when a PR or sequence of commits causes sustained regression.
- Tag performance-tracking issues with `area/tests` and the relevant subsystem
  label (for example, `area/compiler`).

## Prioritization

At least once per month, triage outstanding flaky/performance issues and
prioritize:

1. Highest-frequency failures.
2. Failures impacting smoke validation paths.
3. Regressions affecting multiple platforms.

The top-priority subset should be assigned for near-term stabilization work.
