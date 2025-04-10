# Reinforcement Learning: Ten-Armed Testbed

## Project Overview

This repository contains an implementation of the Ten-Armed Testbed problem, an essential scenario in reinforcement learning to understand and evaluate action selection strategies such as epsilon-greedy, optimistic initial values, and upper-confidence-bound (UCB) methods. The Ten-Armed Testbed provides a simplified yet insightful environment to investigate fundamental reinforcement learning algorithms and decision-making processes under uncertainty.


## Key Concepts

- **Multi-Armed Bandit Problem**: A scenario in reinforcement learning where a fixed limited set of resources must be allocated between competing choices in a way that maximizes expected gain.
- **Action Selection Methods**: Algorithms used to select actions that balance exploration (trying out new actions) and exploitation (using known actions that provide good returns).
- **ε-greedy strategy**: A method where the best-known action is selected with probability 1 - ε, and a random action is chosen with probability ε to encourage exploration.
- **Optimistic Initial Values**: A strategy that assigns high initial values to encourage exploration in early stages.
- **Upper-Confidence-Bound (UCB)**: An approach that selects actions based on both the estimated value and the uncertainty or confidence of those estimates, promoting informed exploration.

## Requirements

- Python 3.x
- numpy
- matplotlib

## Installation

Clone this repository and install the necessary packages using:

```bash
git clone https://github.com/AraratDavtyan/Reinforcement-Learning.git
cd Reinforcement-Learning/Ten-Armed-Testbed
pip install -r requirements.txt
```

## Usage

Run the main file `ten_armed_testbed.py` to execute simulations:

```bash
python ten_armed_testbed.py
```

This script performs experiments comparing different action selection methods and visualizes their average rewards over time. You can adjust the parameters such as the number of steps, arms, and exploration rates to explore different scenarios and understand the implications of these choices on performance.

## Results

The script generates graphs comparing the performance of various strategies, helping to visualize their relative effectiveness in balancing exploration and exploitation. The visualizations include cumulative average rewards, action-value estimates, and confidence intervals, providing comprehensive insights into the dynamics of the algorithms tested.

## Applications

The insights gained from this testbed have broad applications, including recommendation systems, clinical trials, financial decision-making, and online advertisement placements, where decisions must continuously adapt based on incoming data.

## Future Work

Future enhancements for this project could include:

- Implementing additional action selection algorithms.
- Introducing non-stationary environments where the value of arms changes over time.
- Adding interactive visualizations and real-time simulations.
- Extending the testbed to multi-agent scenarios.

## Contributions

Contributions and suggestions for improvements are welcome. Please open an issue or create a pull request to contribute to this project.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

