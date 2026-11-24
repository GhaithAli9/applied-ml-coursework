# Exercise 3 — Linear Regression with Gradient Descent and Step-Length Control

## Overview

Linear regression trained with gradient descent implemented from scratch, comparing a fixed learning rate with two adaptive step-length strategies. Experiments run on the Airfare (`airq402`) dataset and the red and white Wine Quality datasets.

## Techniques used

- Data preparation: shuffling with a fixed seed, train/test splits, handling missing values, encoding categorical columns
- Batch gradient descent for least-squares loss (`minimize_gd`, `learn_linreg_gd`)
- Step-length strategies: fixed step, **Armijo** backtracking line search, and **Bold Driver**
- Convergence and test-error comparison across strategies

## Files

- `notebook.ipynb` — full code with outputs
