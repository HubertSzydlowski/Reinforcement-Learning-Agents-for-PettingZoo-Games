# Reinforcement Learning Agents for PettingZoo Games

## **🧑‍💻 Author**

### Hubert Szydłowski

---

## 🎯 Project Goal

The aim of the project is to implement three artificial intelligence models that use reinforcement learning (RL) to play games available on the PettingZoo platform.

### Selected Games:
- **Rock Paper Scissors**
- **Tic Tac Toe**

The project aims to create and train an RL agent capable of effectively competing against different opponents.

---

## 🪨📄✂️ Rock Paper Scissors (RPS)

The game is played between two players (agent vs. opponent), each choosing one of three symbols: rock, paper, or scissors. The goal is to choose the symbol that beats the opponent's symbol: rock beats scissors, scissors beats paper, and paper beats rock. The game ends with a win, loss, or draw, depending on the choices of both players.

### Opponents:
- **RandomOpponent**: Chooses a move randomly from the available symbols. This is the simplest opponent, with no strategy or learning mechanism.
- **CycleOpponent**: Chooses moves cyclically (e.g., rock, paper, scissors, rock, paper, scissors, etc.). This is a simple opponent that does not respond to the agent's moves.
- **StatisticalOpponent**: Analyzes the history of the agent's moves and chooses the move most often selected in similar situations. It tries to predict and block the agent's preferences.
- **DelayMirrorOpponent**: Chooses the move that was previously selected by the agent but in a mirrored way (e.g., if the agent chose rock, the opponent chooses paper).
- **SmartOpponent**: A Q-learning agent that learns exactly the same way as the main agent. It acts as a dynamic and tough opponent that adapts to the agent's strategy.

### Results:
The agent showed high effectiveness in games against opponents, except for RandomOpponent, which was the hardest due to the randomness of its moves. The best results were achieved in matches against CycleOpponent, where the agent won the vast majority of games. Against more challenging opponents like StatisticalOpponent and DelayMirrorOpponent, the agent maintained an advantage, but had to deal with more difficulties. The number of draws was higher in matches against SmartOpponent, indicating that the agent encountered greater challenges.

---

## ❌⭕️ Tic-Tac-Toe

The game is played on a 3x3 board, where two players alternate placing their symbols: X (player 1) and O (player 2). The goal is to arrange three of your symbols in a line (horizontally, vertically, or diagonally). The game ends with one player's victory or a draw if all the fields are filled and no one has won.

### Opponents:
- **RandomOpponent**: Chooses a random move from the available options, not learning or predicting the agent's moves. This opponent has no strategy.
- **CycleOpponent**: Makes moves in a cyclic order (from 0 to 8), not responding to the agent's moves.
- **StatisticalOpponent**: Analyzes the history of the agent's moves, predicts which move the agent will choose most often, and tries to block it.
- **MirrorOpponent**: Repeats the agent's move, but in the mirrored position on the board (e.g., if the agent selects position 1, the opponent selects position 3). If the move cannot be mirrored, it makes a random move.
- **SmartOpponent**: A Q-learning agent that learns in the same way as the main agent and is the most challenging opponent. The dynamics of the game against this opponent require the agent to adapt its strategies.

### Results:
The agent demonstrated high effectiveness against simpler opponents such as RandomOpponent and CycleOpponent, winning the vast majority of games. Against more advanced opponents like SmartOpponent and MirrorOpponent, the agent had to face greater difficulties but still maintained an advantage, although the number of draws was higher. The agent struggled to predict the moves of SmartOpponent, indicating the adaptability of this opponent.
