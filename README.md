# Handwritten Digit Classification — Logistic Regression & CNN

A beginner machine learning project classifying handwritten digits (0–9) using two models: logistic regression and a convolutional neural network (CNN). Built as a hands-on introduction to both classical ML and deep learning.

## Results

| Model | Test Accuracy |
|---|---|
| Logistic Regression (scikit-learn) | 97.2% |
| CNN (TensorFlow/Keras) | 98.61% |

## Dataset

The [Digits dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html) is built into scikit-learn. It contains:
- 1,797 samples of handwritten digits (0–9)
- Each sample is an 8×8 grayscale image, flattened into 64 pixel features
- 10 balanced classes (~180 samples per digit)

## What's Covered

**Logistic Regression**
- Loading and visualizing the dataset
- Train/test split and feature scaling with StandardScaler
- Training a multiclass logistic regression model (One-vs-Rest)
- Evaluating with accuracy, confusion matrix, and classification report
- Visualizing model coefficients to interpret what was learned per digit

**CNN**
- Reshaping data into (samples, height, width, channels) format
- Normalizing pixel values and one-hot encoding labels
- Building a CNN with Conv2D, MaxPooling, Dropout, and Dense layers
- Training with Adam optimizer and categorical crossentropy loss
- Plotting training and validation accuracy/loss curves over epochs

## Key Findings

- The CNN outperformed logistic regression by ~1.4 percentage points
- Both models struggled most with digits 1, 3, 5, and 8 due to their visual similarity
- 6 out of 10 digits reached 100% recall with the CNN
- Training curves showed healthy learning with no significant overfitting
- The performance ceiling is largely due to the low 8×8 resolution of the dataset — not the models

## Requirements
```
scikit-learn
matplotlib
numpy
tensorflow
```

## How to Run

Open the notebook in [Google Colab](https://colab.research.google.com/) — all dependencies come pre-installed. Run cells top to bottom.

## Key Takeaways

Logistic regression sees raw pixels with no spatial awareness. A CNN keeps the image intact and slides filters across it to detect edges, curves, and shapes — that spatial understanding is what makes it better suited for image tasks. The training history plots show both models learning quickly in the first few epochs before plateauing, with validation accuracy staying close to training accuracy throughout — a sign of healthy generalization.

Classifying handwritten digits with logistic regression (97.2%) and a CNN (98.6%) — a beginner ML pipeline from data loading to training, evaluation, and interpretation.
