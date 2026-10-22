# Flaky-Check Drill Notes

This sandbox repo is a hands-on exercise for practicing pull-request hygiene and surviving flaky CI.

## What the drill covers

1. **Open a PR with a deliberately flaky check** — `.github/workflows/flaky-check.yml` fails on the first attempt of any run and passes on every subsequent attempt.
2. **Re-run failed jobs only** — watch the first check go red, then re-run just the failed jobs and see the check recover to green.
3. **Sync with a moving base** — after the default branch advances with a new commit, update the PR branch so the PR stays up to date and mergeable.
4. **Read CI status** — confirm the PR's final status reflects the recovered checks.
5. **Check code scanning** — inspect code scanning alerts on the repo (some setups have none, and that is a valid result).

## Takeaway

A red X on a PR is not always a broken change — some failures are flaky and resolve with a single re-run. Always read the logs before panicking, and keep your branch current with the base.
