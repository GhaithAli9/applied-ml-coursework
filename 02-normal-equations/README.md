# Exercise 2 — Multiple Linear Regression via Normal Equations

## Overview

Multiple linear regression solved by three different numerical methods, implemented from scratch. The exercise uses a real dataset of 101 gas stations (price, pumps, gasoline types, area income) and predicts gas price from the other numeric features.

The three methods all solve the same linear system `Aβ = b` derived from the Normal Equations, but through different numerical routes with different stability and complexity tradeoffs.

## Methods implemented

1. **Gaussian Elimination** — direct forward elimination + back substitution, written manually with augmented matrices.
2. **Cholesky Decomposition** — factors the symmetric positive-definite matrix `A = LLᵀ` and solves in two triangular steps (forward and back substitution).
3. **QR Decomposition** — factors `X = QR` and solves `Rβ = Qᵀy` by back substitution on the upper-triangular `R`.

All three include manually implemented forward and back substitution.

## Key results

- All three methods produce **identical coefficients** (to full floating-point precision), confirming correctness across independent implementations.
- The trained model has an RMSE of $0.078 on the held-out test set — reasonable for a linear model on a small (~100 sample) dataset with only three numeric features.
- Residual analysis reveals higher errors at price extremes (near $1.73 and $1.99) and low errors near the mean price ($1.86) — a characteristic behavior of linear regression that motivates non-linear models for wider price ranges.

## Data analysis

Part 1 of the notebook also includes exploratory analysis with Pandas: numeric summaries, grouping by station brand (revealing Costco's low-price/high-volume strategy vs. Texaco's premium pricing in higher-income areas), boxplots for outlier detection, and min-max normalization of the income feature.

## Techniques used

- Manual matrix algebra: augmented matrices, elimination, substitution
- Numerical linear algebra: Cholesky and QR factorizations
- Design matrix construction with bias column
- Train/test split for out-of-sample evaluation
- Residual analysis and RMSE

## Files

- `notebook.ipynb` — full code with outputs
- `report.pdf` — derivations, methodology, and results
