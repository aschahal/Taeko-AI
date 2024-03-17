# Teeko AI

Based on [original boardgame](https://en.wikipedia.org/wiki/Teeko). The game Teeko was first released in 1945. Teeko is played on a 4x4 grid. The name was changed to Teeko (and the board grid changed to 5x5) for the 1952 release by John Scarne Games.

Each player has four pieces. Players start by alternately placing pieces on a 5x5 grid, then alternate moves (moving one piece each turn to an adjacent point on the grid). Object is to get four pieces in a row, or to form a square with your four pieces.

[Source](Teeko_board.jpg).

## Setup

This project was made entirely in Python.

## Available Scripts

In the project directory, you can run the application to play the game in terminal.

## Make Move

The make_move(self, state) method begins with the current state of the board. Created a heuristic
scoring function to evaluate the "leaves" at depth d, and propagate those
scores back up to the current state, to select and return the best possible next move
using the minimax algorithm.

## 1. Generate Successors

A successor function (e.g. succ(self, state) ) is defined that takes in a board state
and returns a list of the legal successors. During the drop phase, this simply means
adding a new piece of the current player's type to the board; during continued
gameplay, this means moving any one of the current player's pieces to an unoccupied
location on the board, adjacent to that piece.

## 2. Evaluate Successors

Using game_value(self, state) as a starting point, created a function to score
each of the successor states. A terminal state where the AI player wins should have
the maximal positive score (1), and a terminal state where the opponent wins should
have the minimal negative score (-1).

## 3. Implement Minimax

Defined a max_value(self, state, depth) function where the first call
will be max_value(self, curr_state, 0) and every subsequent
recursive call will increase the value of depth.
When the depth counter reaches your tested depth limit OR you find a
terminal state, terminate the recursion.

