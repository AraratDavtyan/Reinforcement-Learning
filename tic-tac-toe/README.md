# Tic-Tac-Toe  

This repository contains an implementation of Tic-Tac-Toe using Reinforcement Learning (RL). The goal of this project is to apply RL techniques to train an agent that can play optimally against human opponents or other AI agents.  

The implementation explores state-value learning, policy optimization, and reward-based decision-making to improve the agent’s performance over time.  

---

## Features  

- Self-learning Agent – The agent learns optimal moves through reinforcement learning.  
- Exploration vs. Exploitation – Balances exploration of new moves and exploitation of learned strategies.  
- Customizable Training – Allows adjustment of learning parameters, reward functions, and exploration rates.  
- Human vs. AI– Play against the trained agent.  

---

## Project Structure  
tic-tac-toe/
│── src/
│   ├── judge.py        
│   ├── player.py 
│   ├── policy_first.bin
│   ├── policy_second.bin
│   ├── state.py        
│   ├── tic_tac_toe.py         
│── README.md            

---

## Getting Started  

### Installation  

1. Clone the repository:  
     git clone https://github.com/AraratDavtyan/tic-tac-toe.git
   cd tic-tac-toe
   2. Install dependencies:  
     pip install -r requirements.txt
   3. Train the AI agent and play against the trained AI:  
     python tic-tac-toe.py
   
---
## References  

This implementation is inspired by concepts from:  

- *Reinforcement Learning: An Introduction* by Richard S. Sutton and Andrew G. Barto (Second Edition, MIT Press, 2018).  

For more details on RL principles, visit: [Sutton & Barto's book](https://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf).  

---

## Libraries and Frameworks Used  

- Python – Core programming language for the project.  
- NumPy – Efficient numerical operations for RL computations.