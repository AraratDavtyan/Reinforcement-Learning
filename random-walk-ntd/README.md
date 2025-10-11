
# Reinforcement Learning: n-step TD on Random Walk

This project implements n-step Temporal Difference (TD) methods to solve the Random Walk problem.  
It is based on Chapter 7: n-step Bootstrapping, specifically Example 7.2, from the book *Reinforcement Learning: An Introduction* by Richard S. Sutton and Andrew G. Barto.

---

## Project Structure

```
random-walk-ntd/
├── src/                     # Core implementation
│   └── random_walk.py       # Logic for n-step TD methods
├── notebooks/               # Jupyter Notebook for experimentation
│   └── random_walk.ipynb
├── book_images/             # Reference images from the book
│   ├── Example_6_2_top.PNG
│   └── Figure_7_2.PNG
├── generated_images/        # Plots generated from simulations
│   └── figure_7_2.png
└── README.md                # Project documentation
```

---

## Key Features

- Implements n-step TD prediction, generalizing TD(0) and Monte Carlo.  
- Uses a 19-state Random Walk environment with terminal rewards.  
- Compares learning performance for different n-step values.  
- Reproduces Sutton’s Figure 7.2 experiment.  
- Modular implementation for use in Python scripts or notebooks.

---

## Environment Overview

- 1D Random Walk with 19 non-terminal states.
    - Terminal states: State 0 (Left) and State 20 (Right)
    - Non-terminal states: States 1–19
- The agent starts from State 10 (middle).
- At each step, the agent randomly moves left or right with equal probability (p=0.5).
- Rewards:
    - Left terminal (State 0) → -1
    - Right terminal (State 20) → +1
    - All other states → 0

### True State Values
Ground truth is a linear ramp between -1 and +1:

```
V(s) = -0.9, -0.8, ..., 0.8, 0.9 for states 1–19
```

---

## Learning Algorithm: n-step TD

### n-step TD Prediction

- Generalizes between TD(0) and Monte Carlo.
    - n = 1 → equivalent to TD(0)
    - n → ∞ → approaches Monte Carlo
- Update rule:  
  ```
  G = R(t+1) + γ * R(t+2) + γ^2 * R(t+3) + ... + γ^(n-1) * R(t+n) + γ^n * V(S(t+n))
  ```
- Balances bias and variance depending on n.

---

## Results and Visualizations

### Figures from Sutton’s Book

These figures illustrate how n-step TD methods behave during learning:

<img src="book_images/Figure_7_2.PNG" alt="Sutton Fig 7.2" width="400"/>
<img src="book_images/Example_6_2_top.PNG" alt="Reference Example" width="400"/>

---

### Generated Simulation Results

<img src="generated_images/figure_7_2.png" alt="n-step TD Results" width="400"/>

These results show how different values of n affect learning speed and accuracy.

---

## Key Observations

- Small n (e.g., 1-step TD) results in more bias but faster updates.  
- Larger n results in less bias but higher variance.  
- Intermediate values of n provide a balance between speed and stability.  
- The implementation reproduces Sutton’s results accurately.

---

## Conclusion

This project demonstrates how n-step TD connects TD(0) and Monte Carlo, and how the choice of n influences learning behavior.  
The Random Walk with n-step TD is a fundamental example for understanding bootstrapping and the tradeoff between bias and variance in reinforcement learning.
