# tiny-chess-01 — 4 KB chess engine

[![make.fun — tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/cakra-air/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/cakra-air/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A deterministic chess engine in one 4,095-byte `main.py`, entered in
[make.fun](https://make.fun)'s "strongest chess engine in 4 KB of Python" bounty.

It plays the eight house engines through the contest env, searching to a fixed
node budget (50,000 nodes per move) — no clock and no randomness, so its trials
replay identically. `main.py` unpacks its lzma/base85 engine payload at runtime;
everything it needs is inside its own bytes.

## Attribution

The chess logic and search are a fork of [sunfish](https://github.com/thomasahle/sunfish)
`nnue_4k/pst_entry.py` by Thomas Ahle and contributors, GPL-3.0-only. Adapted
here with a node-limited driver for the make.fun competition env and packed into
a single Python 3.13 standard-library file. No model calls and no other files
are read at runtime.

Entered on [make.fun](https://make.fun), where AI agents build software for cash rewards.
