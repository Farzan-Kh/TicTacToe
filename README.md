# TicTacToe

A Python implementation of 5x5 Tic-Tac-Toe, featuring an AI opponent that utilizes either the **Minimax** or **Monte-Carlo Tree Search (MCTS)** algorithms. This project was developed for UAF CS605 Artificial Intelligence, Spring 2021.

## Features

- **5x5 Tic-Tac-Toe**: A larger version of the classic game, with unique win conditions.
- **Custom Win Condition**: The game now detects **L shapes** as win states for players, instead of the traditional straight lines or diagonals.
- **AI Opponent**: Play against an AI that can use either the Minimax algorithm with alpha-beta pruning or the Monte-Carlo Tree Search algorithm.
- **Human vs Human**: Play against another human locally.
- **AI vs AI**: Watch two AI players compete against each other.
- **Game Replay**: Replay previously saved games.
- **Game Saving**: Save your game progress to a file and resume later.

## Project Structure

```
.
├── .gitignore
├── LICENSE
├── README.md
└── tictactoe/
    ├── __init__.py
    ├── ai.py
    ├── game.py
    └── tictactoe.py
```

### File Descriptions

- **`tictactoe/tictactoe.py`**: The main entry point for the game. Contains the user interface and handles game modes.
- **`tictactoe/game.py`**: Implements the core game logic, including board rendering, win condition checks (including the new L-shape logic), and game saving.
- **`tictactoe/ai.py`**: Contains the AI logic, including the Minimax algorithm with alpha-beta pruning and the Monte-Carlo Tree Search algorithm.
- **`tictactoe/__init__.py`**: Empty file to mark the directory as a Python package.
- **`.gitignore`**: Specifies files and directories to be ignored by Git, such as virtual environments and cached files.
- **`LICENSE`**: The MIT License under which this project is distributed.
- **`README.md`**: Documentation for the project.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/Farzan-Kh/TicTacToe.git
   cd TicTacToe
   ```

## How to Play

1. Run the game:
   ```sh
   python tictactoe/tictactoe.py
   ```

2. Choose a game mode:
   - **[1] Play a new game**: Start a fresh game.
   - **[2] Continue a game**: Load a previously saved game.
   - **[3] Watch a previously played game**: Replay a saved game.
   - **[4] Exit the game**: Quit the program.

3. If playing against an AI, choose the algorithm:
   - **[1] Minimax**: A deterministic algorithm that evaluates all possible moves.
   - **[2] Monte-Carlo Tree Search**: A probabilistic algorithm that uses simulations to determine the best move.

4. Follow the on-screen instructions to play the game.

## Rules

- The game is played on a 5x5 grid.
- Players take turns placing their marker (`X` or `O`) on an empty cell.
- The game ends when:
  - A player forms a winning **L shape** (e.g., a vertical line with a horizontal line attached).
  - The board is full, resulting in a draw.

## AI Algorithms

### Minimax with Alpha-Beta Pruning
- Explores all possible moves to determine the optimal one.
- Uses alpha-beta pruning to reduce the number of nodes evaluated in the game tree.

### Monte-Carlo Tree Search (MCTS)
- Simulates multiple random games to evaluate the potential of each move.
- Balances exploration and exploitation using the Upper Confidence Bound (UCB) formula.

## Saving and Loading Games

- **Save a game**: Enter `wq` during your turn to save the game and exit.
- **Load a game**: Choose option `[2] Continue a game` and provide the path to the saved file.

## Replay Mode

- Choose option `[3] Watch a previously played game` to replay a saved game.
- The game states will be displayed sequentially with a delay.

## Example Gameplay

```plaintext
Welcome to 5x5 Tic-Tac-Toe!
At this juncture, you have several options:
[1] Play a new game.
[2] Continue a game (requires file input).
[3] Watch a previously played game (requires file input).
[4] Exit the game.
Choose an option 1/2/3/4: 1

Would you like to play against:
[1] A human player.
[2] An AI player.
[3] I'd like to watch two AI players play.
[4] Exit the game.
Please choose either 1, 2, 3, or 4: 2

Which algorithm would you like the AI to use?
[1] Minimax.
[2] Monte-Carlo Tree Search
Please choose either 1 or 2: 1

Based on the state of the board, I can see that it is X's turn.
This is the current board state:
             |       |       |       |      
         X   |   O   |       |       |      
      _______|_______|_______|_______|_______
             |       |       |       |      
         O   |   X   |       |       |      
      _______|_______|_______|_______|_______
             |       |       |       |      
         X   |   O   |       |       |      
      _______|_______|_______|_______|_______
             |       |       |       |      
         O   |   X   |       |       |      
      _______|_______|_______|_______|_______
             |       |       |       |      
         X   |   O   |       |       |      
             |       |       |       |      
```

## License

This project is licensed under the MIT License.

## Acknowledgments

- Developed by Dylan Palmieri for UAF CS605 Artificial Intelligence, Spring 2021.
