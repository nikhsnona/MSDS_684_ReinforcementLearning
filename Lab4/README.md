# **Lab 4 – Temporal-Difference Learning (SARSA & Q-Learning)**

This lab contains the complete implementation for MSDS 684 – Reinforcement Learning, Lab 4. The work focuses on TD(0) control methods in the CliffWalking-v1 environment, comparing on-policy SARSA with off-policy Q-learning.
The lab highlights the behavioral differences between the two methods, the effect of online step-by-step updates, and the importance of exploration in safety vs. optimality tradeoffs.

All experiments are implemented in a Jupyter notebook, with code organized into clear sections for algorithms, multi-seed evaluation, visualizations, and additional hyperparameter studies.



## **Project Contents**

This lab includes full implementations and analysis of:

* SARSA (on-policy TD control)
* Q-learning (off-policy TD control)
* Online TD(0) updates driven by `env.step()`
* ε-greedy action selection with decay scheduling
* Multi-seed statistical evaluation (30 seeds)
* Learning curves with 95% confidence intervals
* Value function heatmaps (`max_a Q(s,a)`)
* Greedy policy visualization via arrow plots
* Sample trajectories showing safe vs. risky navigation
* Hyperparameter studies:

  * Learning-rate variations (α)
  * Exploration schedule comparisons (ε-decay)
  * Greedy-only failure case (ε=0)
* Performance summary table (final reward, best reward, sample efficiency)

These components jointly demonstrate the advantages, risks, and learning characteristics of SARSA and Q-learning under the TD framework.



## **How to Use This Script**

1. Run the main Python file in your environment:

   ```bash
   python lab4.py
   ```
2. All figures are automatically saved into:

   ```
   figures_lab4/
   ```
3. Key results (learning curves, heatmaps, policy maps, trajectories, and hyperparameter experiments) display onscreen and save to disk.
4. Hyperparameters such as α, ε-decay, number of seeds, and number of episodes can be modified directly at the top of the script.
5. Additional experiments run automatically after the main SARSA/Q-learning evaluation.

The script is fully reproducible and produces all outputs required for the Lab 4 report.



## **Dependencies**

Install required packages using:

```
numpy==1.26.4
matplotlib==3.8.0
gymnasium==0.29.1
pygame==2.5.2
typing_extensions>=4.5.0
```

These packages ensure consistent execution of the CliffWalking environment, TD control algorithms, and visualizations.



## **Reproducibility**

* All experiments are evaluated over 30 random seeds for stable mean and confidence interval estimates.
* TD control methods use deterministic NumPy implementations.
* Exploration schedules, α-values, and episode counts are configurable at the top of the script.
* Plots and metrics are saved with seed-independent naming for easy comparison across runs.
* Additional experiments are separated into clearly labeled functions for organized, repeatable testing.



## **Repository Structure**

```
Lab4/
│── lab4.py                      # Main script (SARSA, Q-learning, visualizations) and Additional hyperparameter and exploration studies
│── requirements.txt
│── README.md
│── figures_lab4/                # Saved learning curves, heatmaps, trajectories, extras
```
