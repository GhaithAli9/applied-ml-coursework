# Exercise 1 — Pandas, NumPy, and Simple Linear Regression

## Overview

This exercise covers two parts:

1. **Text processing with Pandas and vectorized computation with NumPy** — parsing raw text from a URL, filtering and counting word frequencies, and validating the Central Limit Theorem empirically through matrix-vector operations.

2. **Simple linear regression implemented three ways** — closed-form solution derived from scratch, `numpy.linalg.lstsq` using SVD, and `sklearn.LinearRegression`. All three are compared on coefficients, execution time, and computational complexity.

## Key results

- **Word frequency analysis:** raw counting produces noisy results (HTML tags, common English words). After lowercasing, punctuation removal, and stopword filtering, the top-10 words reflect the actual document topic.
- **CLT verification:** the empirical mean of 100 samples of the sum vector converged to the theoretical expected value (19.95 measured vs. 20.0 expected).
- **Regression comparison:** all three methods produce identical coefficients. Manual and `np.linalg.lstsq` run in ~30 microseconds; sklearn is ~20× slower on this small dataset due to input validation and API overhead — a cost that is negligible on real-world data sizes.

## Techniques used

- Pandas Series and `value_counts()` for frequency analysis
- Regular expressions for text cleaning
- NumPy vectorized operations and Central Limit Theorem
- Closed-form linear regression (derived from minimizing squared error)
- SVD-based least squares (`numpy.linalg.lstsq`)
- scikit-learn `LinearRegression`
- Effect analysis of forcing regression coefficients to zero

## Files

- `notebook.ipynb` — full code with outputs
- `report.pdf` — mathematical background, methodology, and discussion
