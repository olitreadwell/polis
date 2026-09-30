# compdemocracy/polis context
> refreshed 2026-09-30 | upstream default: edge @ f9223dffe

## Identity & policies
- upstream: compdemocracy/polis, default branch `edge`, primary languages JavaScript/TypeScript + Clojure + Python, English-first (yes; docs/UI in English)
- CLA/DCO: none found (CONTRIBUTING.md is a placeholder: "Expect to see a Contributing Agreement here soon")
- AI-assisted PR policy: unstated (no AI clause in CONTRIBUTING, .github, or templates)
- signed commits required: no
- PR template: none (only .github/ISSUE_TEMPLATE/*; no PULL_REQUEST_TEMPLATE anywhere; org `.github` repo 404s)
- external tracker: GitHub issues/PRs only

## Conventions (verified from merged PRs)
- branch naming: `feat/...` and `fix/<kebab>` dominant in recent merges (e.g. fix/probe-reader-snapshot, feat/poll-indexes)
- commit style: lowercase sentence-style, scope prefix common (`delphi: ...`, `probe box: ...`); small fixes use `fix:`
- CI checks that gate merge: lint.yml, jest-client-admin-test.yml, jest-client-report-test.yml, jest-server-test.yml, python-ci.yml, test-clojure.yml, cypress-tests.yml
- fork CI: Actions enabled on olitreadwell/polis (347 runs); a PR does trigger fork workflows
- outside PRs do merge: typo/doc PRs merged before (e.g. #1988 "Small Typo in the Welcome Text string", #885 "fix: spelling in emoji speech_balloon"); maintainers active, merges daily

## Maintainer picture
- active team pushing to `edge` daily; heavy in-flight work in `delphi/` and `probe box` (avoid those areas)
- responsive to small doc/typo PRs historically

## Issue-area health
- CONTRIBUTING is intentionally minimal; low process overhead, so small self-contained doc/typo PRs are welcome
- avoid delphi/probe-box/math internals (active maintainer churn there)

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-08-26` issue #2690 (a11y) — pr-opened — fork PR #1 (fix/seed-comment-form-labels); fork CI not initialized at the time, verified locally
- `2026-09-25..27` — error — engine/loop runs exited without an agent trace (Ollama web_search rejection era); no PR
- `2026-09-30` — typo bundle (self-found, 10 fixes) — pr-opened — fork PR #36 (fix/typo-cleanup, +10/-10); fork CI green except the pre-existing Coordinator S1/S2 check (red on fork edge @3ee448588 and upstream edge @f9223dffe, unrelated)

## Mined gaps (discovered, not yet attempted)
- `2026-09-30` typos in docs/config/UI text (Millenium, identifed, occured, recieve, contributer, accomodate, miliseconds, overriden, specificying x2) — status: attempted (this run)
- `2026-09-30` code-comment typos in server/src/routes/* and math/src/* (freqently, implictly, queston, separte, lke, ...) — status: proposed (not packed this run; 10-file cap reached)
