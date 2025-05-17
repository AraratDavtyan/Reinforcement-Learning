# Reinforcement Learning Projects

This repository contains multiple Reinforcement Learning (RL) projects, each demonstrating different environments, algorithms, and learning techniques inspired by the textbook **Reinforcement Learning: An Introduction** by Richard S. Sutton and Andrew G. Barto (Second Edition, MIT Press, 2018).

These implementations emphasize building RL agents from scratch using foundational algorithms and are designed to deepen practical understanding of agent behavior, policy evaluation, and exploration strategies.

**Reference**:  
_Reinforcement Learning: An Introduction_, Sutton & Barto (2018)  
[Read Online (PDF)](https://www.andrew.cmu.edu/course/10-703/textbook/BartoSutton.pdf)

---

## Projects Overview

Each project is organized in its own directory and includes a dedicated `README.md` describing its objectives, methodology, and findings. The code is kept modular and focused on clarity to ensure that learning mechanisms and agent-environment interactions are easy to follow and extend.

## Project Structure
```
reinforcement-learning/
│── tic-tac-toe/
│── ten-armed-testbed/
│── gridworld-dp/
│── gridworld-mdp/
│── gambler-problem/
│── blackjack/
│── infinite-variance/
│── random-walk/
│── windy-gridworld/
│── cliff-walking/
│── README.md
```
## Implemented Projects


| Project | Core Focus | Techniques |
|---------|------------|------------|
| [tic-tac-toe](./tic-tac-toe/) | Value Function Approximation in Self-Play | TD(0), ε-greedy, State-Value Updates |
| [ten-armed-testbed](./ten-armed-testbed/) | Action-Value Methods for Stationary Bandits | Sample-Average, Constant Step Size, ε-greedy, UCB, Gradient Bandit |
| [gridworld-dp](./gridworld-dp/) | Policy Evaluation and Improvement | Iterative Policy Evaluation, Policy Iteration |
| [gridworld-mdp](./gridworld-mdp/) | Solving MDPs with Known Models | Planning, Value Iteration |
| [gambler-problem](./gambler-problem/) | Finite-Horizon Dynamic Programming | Value Iteration, Policy Evaluation |
| [blackjack](./blackjack/) | Monte Carlo Prediction and Control | On-policy, Off-policy with Importance Sampling, Exploring Starts |
| [infinite-variance](./infinite-variance/) | Stability in Off-Policy Evaluation | Importance Sampling, Variance Analysis |
| [random-walk](./random-walk/) | Prediction in Markov Processes | Monte Carlo vs TD(0) |
| [windy-gridworld](./windy-gridworld/) | Episodic Control in Stochastic Environments | SARSA, ε-greedy, Environment Shaping |
| [cliff-walking](./cliff-walking/) | Control with Temporal-Difference Methods | SARSA, Q-Learning, Expected SARSA |

Each project includes its own source code and, where applicable, notebooks and experiment results.


Each folder contains:
- A dedicated `README.md` with methodology and key results
- Source code for training, evaluation, and visualization
- Notebooks or plots where applicable

---

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/AraratDavtyan/reinforcement-learning.git
cd reinforcement-learning 
```
2. Navigate to any project:

```bash
cd tic-tac-toe
```
3. Install dependencies (typically NumPy, Matplotlib, tqdm):

```bash
pip install -r requirements.txt  # if present
```
4. Run the training or main file:
```bash
python tic_tac_toe.py
```
## Project Descriptions

- **tic-tac-toe/**  
  TD(0) learning via self-play with state-value function updates. Includes human vs agent gameplay.

- **ten-armed-testbed/**  
  Exploration of action-value methods using ε-greedy, optimistic initialization, UCB, and gradient-based algorithms.

- **gridworld-dp/**  
  Classical policy evaluation and improvement in Gridworld using iterative Dynamic Programming methods.

- **gridworld-mdp/**  
  Gridworld with full MDP formulation solved through planning algorithms such as value and policy iteration.

- **gambler-problem/**  
  Value iteration to compute the optimal policy in a probabilistic betting environment with terminal rewards.

- **blackjack/**  
  Monte Carlo prediction and control with on-policy, off-policy, and exploring starts methods. Based on the Blackjack game.

- **infinite-variance/**  
  Off-policy evaluation showing instability due to high variance in importance sampling.

- **random-walk/**  
  A chain-based Markov process used to compare Monte Carlo and TD(0) prediction methods.

- **windy-gridworld/**  
  Episodic task with stochastic transitions solved using SARSA. Highlights exploration in structured environments.

- **cliff-walking/**  
  Gridworld-based episodic control problem. Compares SARSA, Expected SARSA, and Q-Learning strategies.

---

## Libraries Used

All projects are implemented in **Python 3.x**, relying only on widely-used libraries:

- **NumPy** – Efficient numerical operations and array handling  
- **Matplotlib** – Visualization of value functions, learning curves, and policies  
- **tqdm** – Real-time progress bars for training and evaluation loops  

---

## Learning Focus

This repository emphasizes:

- Implementing core reinforcement learning algorithms from scratch, based on Sutton & Barto’s textbook  
- Understanding the differences between prediction and control, on-policy and off-policy learning  
- Experimenting with value-based methods including TD(0), Monte Carlo, and Dynamic Programming  
- Exploring the impact of exploration strategies like ε-greedy, UCB, and optimism in action-value methods  
- Analyzing convergence behavior, variance in returns, and stability in function approximation  
- Comparing theoretical expectations with empirical results through simulation-based experiments  

---
