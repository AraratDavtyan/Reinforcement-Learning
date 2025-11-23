# Reinforcement Learning: Counter-Examples

This project reproduces Baird’s Counterexample from *Reinforcement Learning: An Introduction* (Sutton & Barto, Chapter 11 — Off-policy Methods with Function Approximation).  
It demonstrates the divergence of off-policy TD(0) with linear function approximation and compares it to stable methods such as TDC, Expected TDC, and Emphatic TD.

---

## Project Structure
```
counter-examples/
├── book_images/
│   ├── Figure_11_1.PNG
│   ├── Figure_11_2.PNG
│   ├── Figure_11_5.PNG
│   └── Figure_11_6.PNG
├── generated_images/
│   └── figure_11_2.png
├── notebooks/
│   ├── bairds_counterexample.ipynb
│   ├── tdc_baird.ipynb
│   └── emphatic_baird.ipynb
├── src/
│   └── counter_example.py
└── README.md
```
---

## Overview

Baird’s 7-state MDP highlights the instability that arises when bootstrapping, off-policy sampling, and linear function approximation interact.  
Semi-gradient TD(0) diverges, while gradient-corrected methods such as TDC (GTD(0)), Expected TDC, and Expected ETD converge.

---

## Core Algorithms

### Off-policy TD(0)
w ← w + α ρ δ x(s)

### TDC (GTD(0))
Two sets of weights:
- w for value function
- v for gradient correction  
Converges by minimizing MSPBE.

### Expected ETD
Uses emphatic weighting (M) to stabilize off-policy learning.

---

## Error Metrics
- RMSVE — Root Mean Square Value Error  
- RMSPBE — Root Mean Square Projected Bellman Error  

These metrics measure divergence and convergence behavior.

---

## Visual References
- Figure_11_1.PNG — Baird’s star diagram
- Figure_11_2.PNG / figure_11_2.png — TD(0) divergence
- Figure_11_5.PNG — TDC stability
- Figure_11_6.PNG — Expected ETD stability

---

## Observations
- Off-policy TD(0) diverges under linear approximation.
- TDC, Expected TDC, and ETD converge reliably.
- RMSVE and RMSPBE clearly show the differences in stability.

---

## Conclusion

This project provides a compact reproduction of Baird’s Counterexample, demonstrating the failure of classic off-policy TD(0) and the stability of gradient-TD and emphatic-TD approaches.  
It serves as a concise reference for understanding divergence and stability issues in off-policy reinforcement learning.