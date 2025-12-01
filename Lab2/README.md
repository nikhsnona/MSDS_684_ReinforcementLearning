# **Lab 2 – Dynamic Programming: Policy & Value Iteration on GridWorld and FrozenLake**

This lab contains the complete implementation for MSDS 684 – Reinforcement Learning, Lab 2. The work focuses on applying classical Dynamic Programming (DP) algorithms—including Policy Evaluation, Policy Iteration, and Value Iteration—to both a custom GridWorld environment and Gymnasium’s FrozenLake-v1.

All experiments are implemented in a Jupyter Notebook, with code structured into clear sections for environment setup, DP algorithms, experiments, visualizations, and additional analyses.



## **Project Contents**

* Custom GridWorldEnv built using the Gymnasium API
* Full DP pipeline:

  * Policy Evaluation (synchronous + in-place)
  * Policy Iteration (improvement + evaluation)
  * Value Iteration (synchronous + in-place)
* Visualization suite:

  * Value function heatmaps
  * Policy quiver plots (arrow diagrams)
  * Convergence curves (max ΔV per sweep vs. iteration and wall-clock time)
* FrozenLake-v1 transition model extraction and DP solution
* Extended analyses (extra experiments):

  * Stochasticity sweep (intended probability 1.0 → 0.2)
  * Terminal reward sensitivity (+1, +2, +5, –1)
  * Step-cost variation (0, –0.01, –0.1)
  * FrozenLake deterministic vs. slippery comparison
* Printed results showing sweeps, final deltas, and sample values for clarity



## **How to Use This Notebook**

1. Open the Jupyter Notebook included in the repository.
2. Run all cells in sequence to reproduce the core lab experiments.
3. The extra experiments are provided in a separate cell section and can be run independently.
4. All visualizations are generated inline, and summary metrics (sweeps, deltas, sample V(s)) are printed for interpretability.
5. Hyperparameters—including discount factor, tolerance, stochasticity, step-cost, and terminal rewards—can be modified directly within the notebook cells.

The notebook is organized so reviewers can follow the full DP workflow, understand the effect of different settings, and reproduce the results shown in the lab report.



## **Dependencies**

Install the required Python packages using the provided `requirements.txt`:

```
numpy>=1.24.0
matplotlib>=3.7.0
gymnasium>=0.29.1
jupyter
```

These packages support the custom GridWorld environment, transition-model handling, DP algorithms, and plotting utilities.



## **Reproducibility**

* All random seeds are set in the notebook for consistent results.
* Environment configurations (obstacles, transition probabilities, reward functions) can be adjusted easily.
* Additional experiments are separated into clearly labeled cells for clean iteration and comparison.
* The notebook automatically organizes outputs into subfolders inside `outputs_dp_lab2/`.



## **Repository Structure**

```
Lab2/
│── Lab2_Dynamic_Programming.ipynb   # Main notebook
│── requirements.txt
│── README.md
│── outputs_dp_lab2/                 # Auto-generated plots and results
│── extras/                          # Additional experiment cells
```

