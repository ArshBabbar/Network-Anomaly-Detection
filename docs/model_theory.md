# Decision Trees & Random Forests Theory
*(Network Anomaly Detection)*

## Overview

This document provides a high-level explanation of the machine learning model used in this project.  
The goal is to explain **how the model works conceptually**, without diving into unnecessary mathematical detail.

The project uses a **Random Forest classifier**, which is an ensemble of multiple **Decision Trees**, to detect anomalous and malicious network traffic.

---

## Decision Trees (High-Level)

A Decision Tree is a supervised learning algorithm that makes predictions by recursively splitting the data based on feature values.

Each internal node represents:
- A decision rule on a feature

Each branch represents:
- The outcome of that decision

Each leaf node represents:
- A final class prediction

Decision Trees are easy to interpret but tend to **overfit** when trained alone, especially on high-dimensional and noisy datasets such as network traffic data.

---

## Random Forests

A Random Forest is an **ensemble learning algorithm** that combines multiple decision trees and aggregates their predictions.

Instead of relying on a single tree, Random Forests:
- Train many trees independently
- Introduce randomness to reduce overfitting
- Use majority voting for final classification

This makes Random Forests more robust and better suited for real-world security datasets.

---

## Key Concepts Behind Random Forests

### 1. Bootstrapping
Each decision tree is trained on a **random subset of the training data sampled with replacement**.

This means:
- Some samples may appear multiple times in a tree
- Some samples may not appear at all

Bootstrapping ensures that each tree learns slightly different patterns, increasing model diversity.

---

### 2. Random Feature Selection (Tree Construction)
At each split in a decision tree:
- Only a **random subset of features** is considered
- The best split is chosen **only from that subset**

This prevents dominant features from controlling every tree and reduces correlation between trees, which improves ensemble performance.

---

### 3. Voting
Each decision tree outputs a class prediction.

The final prediction is determined by:
- **Majority voting** (for classification)

The class with the most votes across all trees is selected as the final output.

---

## Split Criterion: Gini Impurity

Each decision tree evaluates the quality of a split using **Gini impurity**, which measures how mixed the classes are at a node.

In this project:
- Gini impurity is used **implicitly**
- `RandomForestClassifier` from scikit-learn uses **Gini impurity by default**
- No explicit criterion parameter is required

Gini impurity was chosen because it is computationally efficient and performs comparably to entropy on large, high-dimensional datasets.

> Note: Entropy and Information Gain are alternative split criteria, but they were not used in this implementation.

---

## Why Random Forest for Network Anomaly Detection

Random Forests are well suited for this task because they:
- Handle high-dimensional feature spaces effectively
- Are robust to noise and outliers
- Reduce overfitting compared to single decision trees
- Work well with mixed numerical and categorical features

These properties make Random Forests a strong baseline model for intrusion and anomaly detection systems.

---

## Practical Note

While this document explains the theoretical concepts, all model parameters and patterns are **learned automatically from the dataset during training**.
