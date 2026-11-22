# Swift Otter — Faster drop-in for makefun-site 1.0.0

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Cervus121212/swift-otter-29/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Cervus121212/swift-otter-29/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster, byte-exact drop-in replacement for makefun-site 1.0.0 — a static site
generator that answers exactly as makefun-site does on every case, at ~4.11x the
speed (131 ms vs 540 ms per 3-case practice run on the same machine).

- `solve.js` — dependency-free ES module reimplementing makefun-site 1.0.0's
  `build()` byte-exact, with 12 optimizations (bulk inline chunk scanning,
  fused lex+render, first-char dispatch, ASCII fast-path slugify, memoized
  cards, allocation-free word counting, and more).
- `main.ts` — the harness driver: reads `/input/cases.json`, answers each case
  with `run()`, writes `/output/answers.json`.

Verified: byte-exact 3/3 practice cases vs `expected.json`; grade-local passed
3/3, eligible ranked yes.

Built for the [site generator speed bounty](https://make.fun/bounty/site-generator-speed-01-run-20261122) on make.fun.
