# game-of-life 

> A Vue.js project 

## Run

``` bash
#download the project
git clone https://github.com/Ben-Mark/Game-of-life.git

# install dependencies
npm install

# serve with hot reload at localhost
npm run dev

```


### The code 

The vue code contains 4 vue components

Each component interacts via the events-hub, a sibling vue instance where, all events run through this object

Every component has its own template, script and style encapsulated for easier maintenance and readability

Note: Index.html imports the project's build.js and routes the entire logic into app id

### Components
``` bash
components: {
  App,
  Board,
  Controls,
  Cell
}
```

### Components hierarchy 
App contains Board and Controls

Board contains Cell

Cell refers to the 2d board index


### Features

- Randomize board
- Glider gun pattern
- Horizon line pattern
- Edit custom patterns by clearing board


### Algorithm

The algorithm's complexity is O(n*m)*8 
n = rows , m = columns, 8 = the number of maximum cell neighbors
The algorithm allows the cells to look for neighbors also on the other edge of the board
giving this game of life an infinite attribute, 
For each table index
the game of life rules apply to it
if cell is on the edge of the table, the rules apply to its sibling on the opposite edge
end of table iterations
old table state equals to new table state ( = next generation)

Conway's Game of Life
=====================

The Game of Life, also known simply as Life, is a cellular automaton devised by the British mathematician John Horton Conway in 1970.
The "game" is a zero-player game, meaning that its evolution is determined by its initial state, requiring no further input. One interacts with the Game of Life by creating an initial configuration and observing how it evolves.


Rules
-----

The universe of the Game of Life is an infinite two-dimensional orthogonal grid of square cells, each of which is in one of two possible states, alive or dead. Every cell interacts with its eight neighbours, which are the cells that are horizontally, vertically, or diagonally adjacent. At each step in time, the following transitions occur:

Any live cell with fewer than two live neighbours dies, as if caused by under-population.

Any live cell with two or three live neighbours lives on to the next generation.

Any live cell with more than three live neighbours dies, as if by overcrowding.

Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

The initial pattern constitutes the seed of the system. The first generation is created by applying the above rules simultaneously to every cell in the seed—births and deaths occur simultaneously, and the discrete moment at which this happens is sometimes called a tick (in other words, each generation is a pure function of the preceding one). The rules continue to be applied repeatedly to create further generations.
