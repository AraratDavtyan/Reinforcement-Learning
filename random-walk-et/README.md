# Reinforcement Learning: Random Walk with Eligibility Traces

This project implements three eligibility-trace methods from **Chapter
12 --- Eligibility Traces** in *Reinforcement Learning: An Introduction*
by Sutton & Barto\*:

-   Off-line λ-return\
-   TD(λ)\
-   True Online TD(λ)

All methods are evaluated on the **Random Walk** environment,
reproducing the behavior shown in Figures **12.3, 12.6, and 12.8**.

------------------------------------------------------------------------

## Project Structure

    random-walk-et/
    ├── book_images/
    │   ├── Figure_12_3.PNG
    │   ├── Figure_12_6.PNG
    │   └── Figure_12_8.PNG
    ├── generated_images/
    │   ├── figure_12_3.png
    │   ├── figure_12_6.png
    │   └── figure_12_8.png
    ├── notebooks/
    │   └── random_walk.ipynb
    ├── src/
    │   └── random_walk.py
    └── README.md

------------------------------------------------------------------------

## Environment: Random Walk

The environment is the standard **5-state Random Walk**:

-   Non-terminal states: A--E\
-   Terminal states: left (0) and right (+1)\
-   Reward:
    -   +1 when entering the right terminal\
    -   0 otherwise\
-   The true value function is linear between the terminal states.

------------------------------------------------------------------------

## Off-line λ-Return

Off-line λ-return is defined by the forward-view return:

\[ G^`\lambda`{=tex}*t\ =\ (1-`\lambda`{=tex})`\sum`{=tex}*{n=1}^{T-t-1}
`\lambda`{=tex}\^{n-1} G_t\^{(n)} + `\lambda`{=tex}\^{T-t-1} G_t \]

with

\[ G_t\^{(n)} = R\_{t+1} + `\cdots `{=tex}+ R\_{t+n} + V(S\_{t+n}) \]

Updates occur once per episode:

\[ w `\leftarrow `{=tex}w + `\alpha `{=tex}`\sum`{=tex}\_t
`\bigl`{=tex}(G_t\^{(`\lambda`{=tex})} - V(S_t)`\bigr`{=tex}) x(S_t) \]

This method provides the reference forward view.

------------------------------------------------------------------------

## TD(λ)

TD(λ) uses the backward-view accumulating trace:

\[ e_t = `\gamma `{=tex}`\lambda `{=tex}e\_{t-1} + x(S_t) \]

TD error:

\[ `\delta`{=tex}*t = R*{t+1} + `\gamma `{=tex}V(S\_{t+1}) - V(S_t) \]

Update rule:

\[ w\_{t+1} = w_t + `\alpha `{=tex}`\delta`{=tex}\_t e_t \]

Your implementation reproduces the equivalence between the forward view
and backward view shown in **Figure 12.6**.

------------------------------------------------------------------------

## True Online TD(λ)

True Online TD(λ) ensures exact forward--backward equivalence at **every
time step**, not only in expectation.

Dutch trace:

\[ e_t = `\gamma `{=tex}`\lambda `{=tex}e\_{t-1} + x(S_t) -
`\alpha `{=tex}`\gamma `{=tex}`\lambda `{=tex}(e\_{t-1}\^`\top `{=tex}x(S_t))
x(S_t) \]

Update:

\[ w\_{t+1} = w_t + `\alpha`{=tex}(`\delta`{=tex}*t + V(S_t) -
V(S*{t-1})) e_t - `\alpha `{=tex}(V(S_t) - V(S\_{t-1})) x(S_t) \]

This method reproduces the results in **Figure 12.8**.

------------------------------------------------------------------------

## Results

  Book Reference   Generated Plot    Description
  ---------------- ----------------- ------------------------------
  Figure 12.3      figure_12_3.png   Off-line λ-return estimates
  Figure 12.6      figure_12_6.png   Forward vs backward TD(λ)
  Figure 12.8      figure_12_8.png   True Online TD(λ) comparison

------------------------------------------------------------------------

## Book Visualizations

-   `book_images/Figure_12_3.PNG`\
-   `book_images/Figure_12_6.PNG`\
-   `book_images/Figure_12_8.PNG`

## Generated Visualizations

-   `generated_images/figure_12_3.png`\
-   `generated_images/figure_12_6.png`\
-   `generated_images/figure_12_8.png`

------------------------------------------------------------------------

## Key Observations

-   Off-line λ-return defines exact forward-view targets.\
-   TD(λ) approximates these targets through backward traces.\
-   True Online TD(λ) produces exact forward--backward alignment at each
    time step.\
-   Eligibility traces unify one-step TD and Monte Carlo methods.\
-   λ controls the balance between bias and variance.

------------------------------------------------------------------------

## Conclusion

This project reproduces the three main eligibility-trace algorithms from
**Chapter 12** using the Random Walk environment.\
It highlights how **λ-return**, **TD(λ)**, and **True Online TD(λ)**
relate to one another and demonstrates their characteristic behaviors
from Figures **12.3**, **12.6**, and **12.8**.
