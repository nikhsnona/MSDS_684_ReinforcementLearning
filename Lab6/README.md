# **Lab 6 – PyTorch & Actor–Critic Methods**

This repository contains the implementation for MSDS 684 – Reinforcement Learning, Lab 6, focusing on policy gradient algorithms using PyTorch. Both the basic Actor–Critic implementation and an enhanced “Extras” version are included in a single Jupyter Notebook.



## **Project Contents**

### **Core Implementation**

* Gaussian-policy Actor
* TD(0) Critic
* Online Actor–Critic loop
* Inline visualizations for returns and TD error
* Saved training history (`ac_returns.pt`)

### **Extras Version (Improved Stability)**

This extended section adds:

* Reward scaling
* Entropy regularization
* Gradient clipping
* Hyperparameter tuning
* Moving-average smoothing
* Policy entropy tracking

**This version also saves plots directly to disk using `plt.savefig()`**, including:

```
ac_pendulum_returns.png
ac_pendulum_td_error.png
ac_pendulum_entropy.png
```

These files are saved automatically in the **exact same directory as the notebook**.



## **How to Use This Notebook**

1. Open the Jupyter Notebook.
2. Run all cells sequentially.
3. All plots appear inline, and the Extras version **also exports the PNG files above** to the notebook folder.
4. Trained PyTorch models are saved as:

   ```
   actor_pendulum.pt
   critic_pendulum.pt
   ```

   also in the same directory.



## **Dependencies**

```
torch
gymnasium
numpy
matplotlib
typing_extensions
```

---

## **Reproducibility**

* Random seeds set for NumPy and PyTorch
* Results logged directly in notebook
* PNG plots saved automatically in the notebook’s directory
* No additional folders required

---

## **Repository Structure**

```
Lab6/
│── Lab6.ipynb                     # All code in one notebook
│── README.md                      # This file
│── ac_pendulum_returns.png        # Saved by Extras version
│── ac_pendulum_td_error.png
│── ac_pendulum_entropy.png
│── actor_pendulum.pt              # Trained actor
│── critic_pendulum.pt             # Trained critic
│── ac_returns.pt                  # Return list from basic version
```

