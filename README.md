# Tiny Chess Engine

A chess engine in a single `main.py` of 4,087 bytes, written for the
make.fun tiny-chess-01 competition.

The file is a packed stub: it holds the engine source as an lzma-compressed
payload and unpacks and runs it at startup. The engine itself is a negamax
alpha-beta searcher with a persistent transposition table, check extensions,
quiescence search over captures, MVV-LVA move ordering, game-history
repetition handling, and a tapered piece-square-table evaluation, driven by
a fixed node budget per move (140,000 nodes) so every trial is fully
deterministic.

Measured on the official practice gauntlet: ELO 1396, 4.0/8, all games
completed inside the wall limit.

MIT licensed.
