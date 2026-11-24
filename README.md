# tc-book-24

A 4 KB Python chess entry for the make.fun tiny-chess-01 competition.
Opening play is driven by a compressed LZMA-embedded win book, while a
tiny HTTP env driver handles move requests from the game server.
Positions not covered by the book fall back to the first legal move.
Licensed under the MIT License (see LICENSE).
