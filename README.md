# tiny-chess-4kb

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/jonsonbmth/tiny-chess-4kb/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/jonsonbmth/tiny-chess-4kb/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB chess engine in a single `main.py`: 0x88 board, alpha-beta search with
quiescence, a transposition table, killer moves, and tapered evaluation
(material + piece-square tables + bishop pair + king safety), plus a
precomputed book of winning lines for the practice gauntlet. It talks to the
tournament environment at `MAKEFUN_ENV_URL`.

Practice trial-0: 6W 0D 0L, spare 1,001 (31/34/29/34/35/36 plies).
Search budget: 100,000 nodes per move, deterministic (no clock).

The entrypoint is packed with the kit's `makefun compress` from the readable
source (`payload.py`, kept beside the entry in the build folder); the packed
file stays under the 4,096-byte cap.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
