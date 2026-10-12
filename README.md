# Black-Box Bayesian Optimization Capstone

Sequential black-box optimization of 8 synthetic functions (ranging from 2D up to 8D) using Gaussian Processes and Upper Confidence Bound (UCB) acquisition strategy in Python.

## Project Structure
- `notebooks/`: Contains the evaluation notebooks for weekly query submissions.
- `README.md`: Project documentation and strategy tracking.

## Section 1: Project Overview & Real-World Relevance
The Bayesian Black-Box Optimization (BBO) capstone project focuses on systematically searching and optimizing unknown objective functions. Because the analytical form of the target functions is completely hidden, the challenge requires building robust surrogate models to predict performance and guide decision-making efficiently.
- **Real-World Relevance:** Mirrors critical real-world scenarios where analytical gradients are unavailable, such as expensive physical simulations, automated hyperparameter tuning for machine learning models, or complex system configurations.
- **Career Impact:** Builds advanced capabilities in surrogate modeling, uncertainty quantification, and algorithmic decision-making under incomplete knowledge.

## Section 2: Inputs and Outputs
- **Inputs:** Continuous coordinate vectors bounded within a standardized domain between 0.0 and 1.0. Query points are formatted as hyphen-separated 6-decimal float strings (e.g., `1.000000-0.000000` for 2D inputs). Dimensions span from 2D (Functions 1 and 2) up to 8D (Function 8).
- **Outputs:** Real-valued performance signals or target response values returned after evaluating query coordinates against the black-box functions.

## Section 3: Challenge Objectives & Constraints
- **Primary Goal:** Maximize target performance metrics across all eight distinct black-box functions.
- **Constraints:** Limited query budgets per weekly batch, unknown non-linear function structures, and the curse of dimensionality in higher-dimensional search spaces.

## Section 4: Technical Approach & Methodological Summary
- **Surrogate Model:** Gaussian Process (GP) regression with uncertainty estimates (posterior mean and standard deviation).
- **Exploration vs. Exploitation:** Controlled via the UCB acquisition parameter (beta). Early rounds favored broad exploration of untested regions, while later cumulative iterations shifted toward exploitation around high-performing zones while maintaining uncertainty-based sampling.
- **Theoretical Integration (SVMs):** Soft-margin Support Vector Machines (SVMs) can be incorporated to classify high vs. low performance regions with slack variables for noise tolerance, while Radial Basis Function kernel SVMs handle complex non-linear response surfaces.
- **Model Limitations:** GP regression faces cubic computational scaling bottlenecks as sample size grows, and automated lengthscale tuning is essential to manage irrelevant features in higher dimensions.

## Weekly Progress
- **Week 1:** Initialized setup, baseline models, and preliminary function evaluations.
- **Week 2 & 3:** Executed weekly query points across all 8 synthetic functions, tuning UCB exploration parameters, logging convergence metrics in Google Colab, and structuring formal technical reflections.
