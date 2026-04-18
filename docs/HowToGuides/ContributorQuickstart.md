# Contributor Quickstart

This quickstart is a short path for first-day contributions. For full details,
see [GettingStarted.md](/docs/HowToGuides/GettingStarted.md) and
[FirstPullRequest.md](/docs/HowToGuides/FirstPullRequest.md).

## 1) Pick a scoped task

- Prefer a [good first issue](https://github.com/swiftlang/swift/contribute).
- Leave a comment on the issue before starting work.

## 2) Build once, then iterate

- Follow the setup and dependency steps in
  [GettingStarted.md](/docs/HowToGuides/GettingStarted.md).
- Use a debug-oriented build while iterating to reduce turnaround time.

## 3) Make small, reviewable changes

- Keep changes scoped to one problem.
- Add or update tests with your change.
- Split large efforts into a series of independent pull requests.

## 4) Run focused checks locally

Use the commands below as a common baseline:

```sh
# Python lint used by Swift CI
python3 utils/python_lint.py

# Lightweight utility test suites
python3 utils/update_checkout/run_tests.py
python3 utils/swift_build_support/run_tests.py

# Build + test entry points (from the repo root)
utils/build-script --help
utils/run-test -h
```

For targeted compiler tests, prefer `utils/run-test` as documented in
[Testing.md](/docs/Testing.md) and
[GettingStarted.md](/docs/HowToGuides/GettingStarted.md#running-tests).

## 5) Open a pull request

- Fill out the PR template clearly.
- Request review and ask someone with write access to run `@swift-ci` if needed.
- Start with smoke testing unless your change needs broader validation.
