# Bayesian Black-Box Optimization Capstone

Sequential black-box optimization of 8 synthetic functions (2D up to 8D) using Gaussian Process regression and Upper Confidence Bound (UCB) acquisition strategy in Python.

---

## 📂 Project Structure
- `notebooks/`: Contains evaluation notebooks for weekly query submissions, data processing, and technical reflections.

---

## 🚀 Project Overview & Real-World Relevance
This project focuses on systematically searching and optimizing unknown objective functions where analytical gradients are completely hidden. 
* **Real-World Application:** Mirrors complex scenarios like expensive physical simulations, hyperparameter tuning for machine learning models, and automated system configurations.
* **Career Impact:** Demonstrates advanced capabilities in surrogate modeling, uncertainty quantification, and decision-making under incomplete knowledge.

---

## 📊 Inputs & Outputs
* **Inputs:** Continuous coordinate vectors bounded between `0.0` and `1.0`, formatted as hyphen-separated 6-decimal float strings (spanning from 2D up to 8D).
* **Outputs:** Real-valued performance signals returned after evaluating query coordinates against the black-box functions.

---

## 🎯 Objectives & Constraints
* **Goal:** Maximize target performance metrics across eight distinct black-box functions.
* **Constraints:** Strict weekly query budgets, non-linear function structures, and the curse of dimensionality in higher-dimensional search spaces.

---

## ⚙️ Technical Approach & Methodology
* **Surrogate Model:** Gaussian Process (GP) regression providing posterior mean predictions and uncertainty estimates (standard deviation).
* **Exploration vs. Exploitation:** Managed via the UCB acquisition parameter (`beta`), shifting from broad exploration in early rounds to targeted exploitation around high-performing zones.
* **Theoretical Integration:** Explored the use of soft-margin Support Vector Machines (SVMs) with slack variables for classifying high vs. low performance regions, and Radial Basis Function kernels for non-linear response surfaces.
* **Model Limitations:** Accounted for cubic computational scaling bottlenecks ($\mathcal{O}(N^3)$) as sample sizes grow and the necessity of automated lengthscale tuning for high-dimensional features.

---

* **Week 1:** Setup, baseline models, and initial exploration.
* **Weeks 2 & 3:** Executed weekly query points across all 8 functions, tuned UCB parameters, and structured technical reflections.
* **Week 4:** Generated and submitted Week 4 query points using the cumulative Gaussian Process model, appended new evaluation results, and completed module reflections and documentation.

