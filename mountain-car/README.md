# Reinforcement Learning: Mountain Car — Semi-gradient n-step Sarsa with Tile Coding

This project implements the **Semi-gradient n-step Sarsa** algorithm with **Tile Coding** for the continuous-state **Mountain Car** problem.  
It reproduces the experiments from *Reinforcement Learning: An Introduction* (Sutton & Barto, Chapter 10 — Function Approximation).

---

## Overview

The Mountain Car environment features an underpowered car that must first move away from the goal to gather enough momentum to reach the top of a hill.  
Because the state space is continuous, the action-value function \( Q(s,a) \) is approximated using **Tile Coding**, which allows local generalization.

---

## Project Structure
```
mountain-car/
├── book_images/
│   ├── Figure_10_1.PNG
│   ├── Figure_10_1_upper_left.PNG
│   ├── Figure_10-2.PNG
│   ├── Figure_10_3.PNG
│   └── Figure_10_4.PNG
├── generated_images/
│   ├── figure_10_1.png
│   ├── figure_10_2.png
│   ├── figure_10_3.png
│   └── figure_10_4.png
├── notebooks/
│   └── mountain_car.ipynb
├── src/
│   ├── mountain_car.py
│   └── tile_coding.py
└── README.md
```

---

## Implementation Details

- **Semi-gradient n-step Sarsa** algorithm for continuous control  
- **Tile Coding** used to approximate \( Q(s,a) \)  
- Reproduces qualitative trends from Sutton & Barto (Figures 10.1–10.4)  
- Includes cost-to-go surface visualizations and parameter variation experiments  

The update follows:

\[
w \leftarrow w + \alpha \bigl(G_t^{(n)} - Q(S_t, A_t)\bigr)
\]
\[
G_t^{(n)} = R_{t+1} + \dots + R_{t+n} + Q(S_{t+n}, A_{t+n})
\]

---

## Results

Generated plots correspond to the book’s figures:

- **figure_10_1.png** — Cost-to-go visualization  
- **figure_10_2.png** — Effect of number of tilings  
- **figure_10_3.png** — Learning curves for different n  
- **figure_10_4.png** — Performance comparison by step size  

These results align with the expected learning behavior described in the book.

---

## Observations

- Tile Coding provides generalization in continuous environments  
- Larger n values stabilize learning but slow early improvement  
- Proper tuning of tilings and step size significantly affects performance  

---

## Conclusion

This project demonstrates how **function approximation** and **multi-step updates** interact in continuous control.  
It serves as a compact and extendable baseline for further research on:

- Eligibility traces (λ-return)  
- Actor–critic methods  
- Continuous-action policy gradients  
