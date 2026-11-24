# Exercise 10 — Support Vector Machines

## Overview

Support vector machines for spam detection on two datasets: Spambase (numeric features) and the SMS Spam Collection (raw text).

## Techniques used

- Exporting data to LIBSVM format
- RBF-kernel SVM with tuning of `C` using stratified cross-validation
- Text features with TF-IDF (`TfidfVectorizer`) in scikit-learn pipelines
- Linear and RBF kernel SVMs compared with logistic regression
- Confusion matrices and classification reports

## Files

- `notebook.ipynb` — full code with outputs
