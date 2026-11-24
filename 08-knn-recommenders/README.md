# Exercise 8 — k-Nearest Neighbours and kNN Recommenders

## Overview

k-nearest-neighbour classification implemented from scratch, followed by user-based and item-based kNN collaborative filtering on the MovieLens 100k dataset.

## Techniques used

- Euclidean distance and efficient top-k neighbour selection (sorted insertion, partial `argmin_k`)
- Single and batched kNN prediction on Iris, with a search over K
- Comparison with scikit-learn `KNeighborsClassifier` on Wine Quality, including timing
- Cosine-similarity matrices for **user-based** and **item-based** collaborative filtering
- Rating prediction evaluated with RMSE

## Files

- `notebook.ipynb` — full code with outputs
