# **Lab 1 – Multi-Armed Bandits & MDP Foundations**

This lab contains the complete implementation for **MSDS 684 – Reinforcement Learning, Lab 1**. The work focuses on exploring the exploration–exploitation tradeoff through multi-armed bandit algorithms and early MDP analysis using Gymnasium environments.

All experiments are implemented in a **Jupyter Notebook**, with code organized into clear sections for environments, agents, experiments, visualizations, and additional tests.

## **Project Contents**

* Custom 10-armed Gaussian bandit environment
* ε-greedy and UCB agent implementations
* Full experiment workflow (1,000 runs × 2,000 steps)
* Plots for average reward and optimal action percentage
* Additional exploration experiments (ε, UCB, arm sizes, non-stationary bandit)
* Gymnasium environment analysis (FrozenLake, Taxi)
* Random policy evaluation for baseline comparison

## **How to Use This Notebook**

1. Open the Jupyter Notebook included in the repository.
2. Run all cells in order, or execute sections individually as needed.
3. All plots are generated inline, and extended experiments are grouped in clearly labeled cells.
4. Adjust hyperparameters directly in the notebook to explore different behaviors.

The notebook is structured so reviewers can step through the full workflow and reproduce the results shown in the lab report.

## **Dependencies**

Install the required Python packages using the provided `requirements.txt`:

numpy==1.26.4
matplotlib==3.8.0
gymnasium==0.29.1
pygame==2.5.2
typing_extensions>=4.5.0

These packages ensure the bandit environment, agents, Gymnasium tasks, and visualizations run consistently.

## **Reproducibility**

* All random seeds are set inside the notebook for consistent results.
* Experiment settings (ε values, UCB constants, number of arms, drift settings) can be modified directly.
* Additional experiments are placed in separate cells to keep the workflow organized and repeatable.

## **Repository Structure**

Lab1/
│── Lab1.ipynb                    # Main notebook
│── requirements.txt
│── README.md
│── plots/                        # Generated visualizations 
│── extras/                       # Additional experiments 
