
# Black-Box Bayesian Optimization Capstone

Sequential black-box optimization of 8 synthetic functions using Gaussian Processes and Upper Confidence Bound (UCB) acquisition strategy in Python.

## Project Structure
- `notebooks/`: Contains the evaluation notebooks for weekly query submissions.
- `README.md`: Project documentation and strategy tracking.

## Methodological Summary
- **Surrogate Model:** Gaussian Process (GP) regression with Matérn 2.5 ARD kernel.
- **Acquisition Function:** Upper Confidence Bound (UCB) balancing exploration and exploitation.
- **Optimization:** Multi-start L-BFGS-B optimization over bounded hypercubes.

## Weekly Progress
- **Week 1:** Initialized setup, baseline models, and preliminary function evaluations.
- Week 2: Executed weekly query points across all 8 synthetic functions, tuning UCB exploration parameters and logging convergence metrics in Google Colab.
