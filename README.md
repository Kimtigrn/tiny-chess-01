# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Kimtigrn/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Kimtigrn/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB chess engine for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty. `main.py` is the whole engine: a 0x88 alpha-beta search with iterative deepening to a fixed 80,000 nodes per move, quiescence, transposition table, null-move pruning, late-move reductions, principal-variation search, killer/history move ordering, and a material + piece-square evaluation. Deterministic: no clock, no unseeded randomness. Python 3.13 standard library only.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

`main.py` is the kit's `makefun compress` packing of the readable source (kept with the build, not committed). Run it with `MAKEFUN_ENV_URL` set to the trial env; it plays the gauntlet over HTTP.

Practice results on the kit's real house env (packed entry, 6-game trials): trial 0: **1,545 Elo** (4W-1D-1L); trial 1: **1,654 Elo** (4W-2D-0L); mean ~1,600 vs the sunfish house baseline's ~1,407 on the same trials. Practice floor to enter the final is 1,154.

---

Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards
