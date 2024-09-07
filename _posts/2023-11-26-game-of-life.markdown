---
layout: post
title:  "Making Conway's game of life in C++"
date:   2023-11-26 20:00:00 +0300
---
```
Under construction...
```

The game of life is a no-player [undecidable turing-complete][1] game with the following rules:
- A live cell with less than two neighbours dies (as if by underpopulation).
- A live cell with two or three neighboors live on to the next generation.
- A live cell with more than three neighbours dies (as if by overpopulation).
- A dead cell with exactly three live neighbours is reborn (as if by reproduction).

It is envisioned running in a 2D orthogonal grid universe which expands to infinity. But for the scope of this implementation, we'll have to limit ourselves in the non-infinite amount of resources we possess in the real world. Therefore, we will shrink Conway's Universe to a 211x56 matrix which can fit up to 11,816 cells.

<p align="center">
  <img src="/resources/gameoflife.gif" width=100 alt="Alt Text">
</p><p align="center">(example)</p>

# Classes:

- Cell: A cell object will be consisted of functions that let us know its living state (if it is alive or not), the total neighbours it currently has, `get` and `set` functions, and the respective constructor and destructor.
- Game: It will contain information such as at which generation we currently are and what the board looks like. When the user configures the initial state and runs the game, it will enter a loop where, in combination with `get` and `set` cell functions, it repeats the following algorithm:
    - Step 1: Check if there is a cell which must die as if by underpopulation. If there is, kill it and go to step 1.
    - Step 2: Check if there is a cell which must die as if by underpopulation. If there is, kill it and go to step 1.
    - Step 3: Check if there is a cell which must be reborn as if by reproduction. If there is, reborn it and go to step 1.
    - Step 4: Inform the user that the game of life has ended. 

[1]: https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life#Undecidability