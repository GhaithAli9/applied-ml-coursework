# Exercise 9 — Matrix Factorization for Recommender Systems

## Overview

Rating prediction on MovieLens 100k with latent-factor models. A matrix factorization model trained with SGD is implemented from scratch and compared against scikit-learn's NMF.

## Techniques used

- Exploratory analysis of users (age distribution, gender split, occupations)
- Matrix factorization `R ≈ PQᵀ` with L2 regularization, trained by stochastic gradient descent
- Mean-centering of ratings, and a 3-fold cross-validated grid search over latent dimension, learning rate and regularization (also for NMF)
- Comparison with scikit-learn `NMF` (coordinate descent)
- Training and validation RMSE curves

## Files

- `notebook.ipynb` — full code with outputs
