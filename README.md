# Tic-Tac-Toe Game

This is a simple console-based implementation of the classic Tic-Tac-Toe game. The game is played by two players who take turns marking the spaces in a 3×3 grid. The player who succeeds in placing three of their marks in a horizontal, vertical, or diagonal row is the winner.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Gameplay Instructions](#gameplay-instructions)
- [Code Overview](#code-overview)
- [License](#license)

## Features

- Two-player game (Player X and Player O)
- Simple console-based user interface
- Input validation to prevent overwriting moves
- Automatic detection of game win or draw conditions

## Installation

1. Clone the repository or download the code files.

    ```sh
    git clone https://github.com/tictactoe.git
    cd tictactoe
    ```

2. Ensure you have Python installed (Python 3.6 or higher is recommended).

3. Run the game:

    ```sh
    python tictactoe.py
    ```

## Usage

1. Run the Python script `tictactoe.py`.
2. Follow the on-screen instructions to play the game.

## Gameplay Instructions

1. Upon starting the game, you will see a welcome message and an instruction board indicating the positions numbered 1 to 9.
2. Player X starts the game.
3. Enter the position number where you want to place your mark (X or O).
4. The game board will be updated and displayed after each move.
5. The game will continue until a player wins or there are no free positions left on the board.
6. If a player wins, a congratulatory message will be displayed.
7. If the board is full with no winner, a message indicating the game is a draw will be displayed.

## Code Overview

### Global Variables

- `board`: A list representing the 3x3 game board.
- `info_board`: A list representing the board with position numbers for reference.
- `currentPlayer`: A variable to keep track of the current player ('X' or 'O').
- `gameOn`: A boolean variable to control the game loop.

### Functions

- `welcome(info_board)`: Displays the welcome message and instructions.
- `printBoard(board)`: Prints the current state of the game board.
- `takePlayerinput(board)`: Takes and validates the player's input.
- `switchPlayer()`: Switches the turn between players X and O.
- `checkrows(board)`: Checks if any row has three identical marks.
- `checkcolumns(board)`: Checks if any column has three identical marks.
- `checkDiagonal(board)`: Checks if any diagonal has three identical marks.
- `checkWinner()`: Checks for a winner and updates the game status.
- `board_full(board)`: Checks if the board is full and updates the game status.

### Main Game Loop

The main game loop continuously checks for a full board and a winner, takes player input, switches the player, and prints the updated board until the game is over.

```python
welcome(info_board)
while gameOn:
    board_full(board)
    checkWinner()
    if gameOn:
        takePlayerinput(board)
    switchPlayer()
    printBoard(board)
