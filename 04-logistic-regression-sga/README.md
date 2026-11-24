# Exercise 4 — Logistic Regression with Stochastic Gradient Ascent

## Overview

Logistic regression implemented from scratch and trained by stochastic gradient ascent on the log-likelihood. Uses the Bank Marketing and Occupancy Detection datasets (UCI).

## Techniques used

- Preprocessing: mapping binary columns, one-hot encoding categorical columns (with `unknown` kept as its own category), normalization using training statistics only, bias column
- Numerically stable log-likelihood and log-loss
- Stochastic gradient ascent with **Bold Driver** step-length adaptation, compared against SGD on log-loss
- **AdaGrad** adaptive learning rates compared against Bold Driver
- Comparison with scikit-learn `LogisticRegression`

## Files

- `notebook.ipynb` — full code with outputs
