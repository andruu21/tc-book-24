# tc-book-24

A Python chess entry for the make.fun tiny-chess-01 competition, under the 4096-byte limit.

Plays from a compressed LZMA win book of deterministic house-engine opening lines, decompressed in memory at startup.

Falls back to a small urllib-based environment driver to fetch game state and submit moves.

Deterministic play: identical positions always yield identical moves.

MIT licensed.
