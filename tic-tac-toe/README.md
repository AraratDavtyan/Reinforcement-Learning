# Reinforcement Learning in Tic-Tac-Toe

This project implements **Reinforcement Learning agents** trained to play **Tic-Tac-Toe** using **state-value estimation** and **temporal-difference learning**. 

The RL agent learns to play against itself, and can then compete with another RL agent or even a human.

---

## Project Structure
```
tic-tac-toe/
│── src/ # Core components for game logic and RL agent
│ ├── state.py # Game state and environment representation
│ ├── player.py # RL and human player implementations
│ ├── judge.py # Game controller to manage turns and evaluate outcome
│ ├── tic_tac_toe.py # Training, evaluation, and play routines
│ ├── policy_first.bin # Saved policy for player 1
│ ├── policy_second.bin # Saved policy for player 2
│── README.md # Project documentation
```


---

## Overview of the System

### RL Approach

The system uses the **TD(0)** method to estimate the value of each state:
- Trains two RL agents using self-play.
- Learns to predict the probability of winning for any board configuration.
- Updates values using:
```
V(S_t) ← V(S_t) + α [V(S_{t+1}) − V(S_t)]
```


Only when greedy actions are taken.

### Key Concepts Used

- **State Hashing**: Every board configuration is uniquely hashed for fast lookup and value storage.
- **ε-Greedy Strategy**: Balances exploration and exploitation during training.
- **Temporal Difference (TD) Learning**: Updates values step-by-step without waiting for the final outcome.
- **Self-Play**: Agents train by playing against each other with random starting positions.
- **Policy Saving**: Trained policies are persisted and can be loaded later for evaluation or gameplay.

---

## Features

-  **Trainable Agents** using TD(0) learning
-  **Autonomous Learning** through self-play
-  **Play against RL agent** in a terminal-based game
-  **Policy Persistence** for reloading trained agents
-  **Human vs AI gameplay** with keyboard-based input

---

## Example Outputs

### During Training
```
Epoch 5000, Player1 Win Rate: 0.53, Player2 Win Rate: 0.47
Epoch 10000, Player1 Win Rate: 0.56, Player2 Win Rate: 0.44
```


### Human Gameplay
```
| 0 | 0 | 0 |
| 0 | * | x |
| x | * | * |
RL player wins!
```


---


## Extensions & Future Work
- Incorporate Q-learning for action-value based learning

- Extend to larger board sizes (e.g. 4x4 or 5x5)

- Use function approximation for continuous board states

- Add GUI or Web-based interface for gameplay

---
