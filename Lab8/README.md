# MSDS 684 – Week 8 Capstone

## Modern Deep Reinforcement Learning (Option C: PPO)

This repository contains the final capstone project for MSDS 684 – Reinforcement Learning, focusing on connecting foundational RL concepts to modern deep reinforcement learning using Proximal Policy Optimization (PPO).

The goal of this project is not just to apply a deep RL library, but to **understand why modern algorithms work**, how they relate to classical methods from Sutton & Barto, and which engineering choices meaningfully affect performance.



## Project Overview

In this project, I applied Proximal Policy Optimization (PPO) from the Stable-Baselines3 library to the CartPole-v1 environment. CartPole requires function approximation and serves as a clean benchmark for studying policy-gradient methods in practice.

The project includes:

* A baseline PPO implementation
* Systematic hyperparameter experiments
* Simple ablation studies
* Quantitative evaluation with mean ± standard deviation
* Analysis connecting theory to practice



## Environment

* Environment: CartPole-v1 (Gymnasium)
* Observation Space: Continuous (4-dimensional)
* Action Space: Discrete (2 actions)
* Why CartPole:

  * Requires function approximation
  * Cannot be reliably solved with tabular methods
  * Fast to train, ideal for controlled experiments



## Code Structure


.
├── notebook.ipynb              # Main Jupyter notebook (all experiments)
├── option_c_results/
│   ├── figures/
│   │   ├── learning_curves.png
│   │   └── final_performance.png
│   └── summary.csv
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```



## Experiments Conducted

### 1. Baseline PPO

* PPO with default Stable-Baselines3 settings
* MLP policy network
* Vectorized environments for efficient rollout collection

### 2. Hyperparameter Sensitivity

Systematic evaluation of:

* Learning rate: `1e-4`, `3e-4`, `1e-3`
* Network architectures: `[64, 64]`, `[128, 128]`

Learning curves were generated to visualize convergence behavior across configurations.

### 3. Ablation Studies

Minimal one-parameter changes to isolate effects:

* Batch size: 64 vs. 256
* Entropy coefficient: 0.0 vs. 0.01

Each ablation reports mean ± standard deviation over multiple evaluation episodes.



## Key Engineering Techniques

The following PPO design choices were critical for stability and performance:

* Clipped policy objective to prevent destructive updates
* Advantage estimation (GAE) to reduce variance
* Value function baseline to stabilize gradients
* Mini-batch optimization for efficient and robust updates
* Deterministic evaluation to fairly assess learned policies

These techniques directly address the high variance and instability seen in earlier policy-gradient methods such as REINFORCE.



## Results Summary

* PPO consistently solved CartPole-v1 within 30,000 timesteps
* Performance was robust across a wide hyperparameter range
* Smaller batch sizes led to more stable learning
* Excess entropy regularization slightly reduced final performance on this simple task

All results are visualized and saved in the `option_c_results/` directory.



## Requirements

Install dependencies using:

```bash
pip install stable-baselines3 gymnasium numpy pandas matplotlib
```



## Academic Integrity & AI Use

External resources such as official documentation, research papers, and AI-assisted tools (including ChatGPT) were used for learning, debugging, and conceptual clarification.
All experiments, code execution, analysis, and interpretations reflect my own work and understanding.



## References

* Sutton, R. S., & Barto, A. G. (2018). Reinforcement Learning: An Introduction
* Schulman et al. (2017). Proximal Policy Optimization Algorithms
* Stable-Baselines3 Documentation
* Gymnasium Documentation
