# tc-book-24
A <=4096-byte Python chess engine for make.fun tiny-chess-01, MIT licensed.
Embeds an LZMA-compressed win book of deterministic house-engine lines (24 openings).
Drives make.fun's env over HTTP with `urllib`: `POST /game` to poll, `POST /move` to reply.
Book row = `opponent_index * 24 + opening_index`; moves replay from a byte-packed line table.
Payload is a raw LZMA1 literal decoded at startup; stdlib only (`lzma`, `os`, `urllib`, `json`).
Single file `main.py` with no external chess libraries — see [LICENSE](LICENSE) for MIT text.
Book lines are win lines indexed by opponent engine config and opening id; play is deterministic.
