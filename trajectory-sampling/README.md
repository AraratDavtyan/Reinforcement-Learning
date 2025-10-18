# Trajectory Sampling

This project explores **trajectory sampling** as a method for distributing updates in **model-based reinforcement learning**.  

---

## Project Structure

```
trajectory-sampling/
├── src/ # Implementation of update strategies
│ └── trajectory_sampling.py
├── notebooks/ # Jupyter notebook for experiments
│ └── trajectory_sampling.ipynb
├── book_images/ # Reference figures from Sutton & Barto
│ ├── Figure_8_8_1.PNG
│ └── Figure_8_8_2.PNG
├── generated_images/ # Simulation outputs
│ └── figure_8_8.png
└── README.md
```


---

## Overview

- Compares **uniform** and **on-policy (trajectory)** update distributions
- Uses **expected updates** to study planning efficiency
- Evaluates **policy quality** via the value of the start state
- Demonstrates how update focus affects **learning speed and convergence**

---

## Results

Reproduction of Sutton’s Figure 8.8 comparing uniform and trajectory sampling:

<img src="generated_images/figure_8_8.png" width="400"/>

---

## Conclusion

- **Trajectory Sampling:** faster early learning; focuses on relevant states
- **Uniform Sampling:** slower initially but ensures full convergence

The experiment illustrates the trade-off between **focused** and **comprehensive** update strategies in planning for reinforcement learning.
