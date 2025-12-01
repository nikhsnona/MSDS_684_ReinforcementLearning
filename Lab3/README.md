# **Lab 3 – Monte Carlo Control in Blackjack**

This repository contains the complete implementation for MSDS 684 – Reinforcement Learning, Lab 3. The work focuses on applying First-Visit Monte Carlo Control to the Blackjack-v1 environment and analyzing how exploration settings, discount factors, and initialization choices influence learning.

All experiments are implemented in Python (Jupyter Notebook or script), with code organized into clear sections for episode generation, MC updates, policy improvement, plots, and extended experiments.



## **Project Contents**

* First-Visit Monte Carlo Control implementation
* ε-soft on-policy action selection
* Complete episode generation using Gymnasium
* 3D value function visualizations

  * Usable Ace
  * No Usable Ace
* Learning curve for 500,000-episode training run
* ε-schedule experiments (0.01, 0.1, linear decay)
* Additional experiments:

  * γ variations (0.8, 0.9)
  * Optimistic initialization
  * Short vs. long training horizon
  * Extreme ε = 0.001 exploration test
* Automatic figure saving to a dedicated folder

These components reproduce all results presented in the Lab 3 report.



## **How to Use This Project**

1. Open the notebook or run the main Python script.
2. Execute all sections in order to generate value surfaces, learning curves, and experiments.
3. All plots are saved automatically inside the `lab3_mc_blackjack_figs/` folder.
4. Hyperparameters (ε, γ, number of episodes, initialization values) can be modified at the top of the script to explore different behaviors.

The workflow is structured so reviewers can easily reproduce every result from start to finish.



## **Dependencies**

Install all required Python packages using the provided `requirements.txt`:

```
gymnasium==0.29.1
numpy
matplotlib
```

These packages ensure that Blackjack, Monte Carlo updates, and visualization tools run consistently.



## **Reproducibility**

* Random seeds are set for stable and repeatable results.
* Episode generation, return computation, and policy updates follow the same sequence across runs.
* Additional experiments (γ tests, optimistic initialization, ε extremes) are separated into clearly labeled sections for clarity.
* All figures are created programmatically and stored for documentation.



## **Repository Structure**

```
Lab3/
│── lab3.py                           # Main MC Control implementation and Additional experiments
│── requirements.txt
│── README.md
│── lab3_mc_blackjack_figs/           # Generated figures
│     ├── value_function_usable_ace.png
│     ├── value_function_no_usable_ace.png
│     ├── learning_curve_main.png
│     ├── learning_curves_eps_experiments.png
│     ├── exp_gamma_comparison.png
│     ├── exp_optimistic_init.png
│     ├── exp_horizon_comparison.png
│     └── exp_extreme_epsilon.png
```
