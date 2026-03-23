# Digit-recognizer-with-logistic-regression

# Handwritten Digit Classification with Logistic Regression

A beginner machine learning project using logistic regression to classify handwritten digits (0–9) from the scikit-learn Digits dataset.

## Overview

This project walks through a complete ML pipeline — from loading and exploring data to training a model and interpreting what it learned. Built as a hands-on introduction to logistic regression and scikit-learn.

**Result: 97.2% test accuracy**

## Dataset

The Digits dataset is built into scikit-learn. It contains 1,797 samples of handwritten digits (0–9), where each sample is an 8×8 grayscale image flattened into 64 pixel features, with 10 balanced classes (~180 samples each).

## What's Covered

- Loading and visualizing the dataset
- Train/test split and feature scaling with `StandardScaler`
- Training a multiclass logistic regression model (One-vs-Rest)
- Evaluating with accuracy, confusion matrix, and classification report
- Visualizing model coefficients to interpret what was learned per digit

## Results

| Metric | Score |
|---|---|
| Test Accuracy | 97.2% |
| Most confused pair | 3 vs 8 |

## Requirements
```
scikit-learn
matplotlib
numpy
```

## How to Run

Open the notebook in [Google Colab](https://colab.research.google.com/) or any Jupyter environment. All dependencies come pre-installed in Colab — just run the cells top to bottom.

## Key Takeaway

By visualizing the model's coefficients reshaped into 8×8 images, you can literally see what pixel patterns the model learned to associate with each digit — a great illustration of interpretability in linear models.
