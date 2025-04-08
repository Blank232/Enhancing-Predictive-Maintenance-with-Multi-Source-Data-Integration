# 📊 Enhancing Predictive Maintenance with Multi Source Data Integration

This repository contains a complete machine learning pipeline for performing predictive maintenance on industrial equipment using multivariate sensor data. The primary goal is to predict equipment failure likelihood based on historical sensor readings by comparing the performance of three widely-used regression models: **Random Forest**, **Support Vector Regressor (SVR)**, and **Gradient Boosting Regressor (GBR)**.

---

## 📌 Project Objective

Predictive maintenance is a critical component of Industry 4.0, aiming to reduce unplanned downtime, optimize repair schedules, and enhance overall operational efficiency. This project:
- Builds and evaluates regression models to predict failure scores.
- Uses robust cross-validation and hyperparameter tuning.
- Visualizes model performance and training behaviors.
- Offers a reproducible and scalable notebook for further research or deployment.

---

## 📁 Dataset Description

The dataset includes sensor readings from various machines with each row representing:
- Numerical sensor values over time.
- A continuous target variable `fail` indicating the degradation/failure likelihood.

### Preprocessing Steps:
- Missing value handling.
- Feature scaling using `StandardScaler`.
- Splitting into training/testing datasets.
- Normalization of features to improve learning stability.

---

## ⚙️ Models Implemented

Three models were trained and tuned using `GridSearchCV`:

### 1. **Random Forest Regressor**
- Bagging ensemble of decision trees.
- Good for interpretability and robustness.
- Tuned parameters: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`.

### 2. **Support Vector Regressor (SVR)**
- Non-linear model using RBF kernel.
- Effective for small to medium datasets.
- Tuned parameters: `C`, `epsilon`, `gamma`, `kernel`.

### 3. **Gradient Boosting Regressor**
- Sequential model using boosting.
- High accuracy and resistance to overfitting.
- Tuned parameters: `learning_rate`, `n_estimators`, `max_depth`, `subsample`.

---

## 🔍 Evaluation Strategy

Evaluation was performed using **5-fold cross-validation** to ensure generalization and reduce overfitting risk.

### Metrics Used:
- **Mean Absolute Error (MAE)** – Average magnitude of errors.
- **Root Mean Squared Error (RMSE)** – Penalizes large errors.
- **R² Score** – Measures variance explained by the model.

---

## 📈 Visual Analysis

The project includes several visualizations to interpret model performance and learning behavior:

### ✅ Metric Comparison Charts
- Bar plots for MAE, RMSE, and R².
- Allow easy side-by-side comparison of model accuracy.

### 📉 Learning Curves
- Show how model performance evolves with increasing training data.
- Help identify overfitting or underfitting trends.

### 🔍 Residual Plots
- Reveal how prediction errors are distributed.
- Check for bias or non-random patterns in predictions.

### 🌟 Feature Importance (Random Forest)
- Highlights key sensor features contributing to predictions.
- Supports domain experts in diagnosing critical sensor inputs.

---

## 📊 Performance Summary

| Model                    | MAE   | RMSE  | R²    |
|--------------------------|-------|-------|-------|
| Random Forest Regressor  | 0.32  | 0.61  | 0.63  |
| Support Vector Regressor | 0.34  | 0.58  | 0.66  |
| Gradient Boosting        | 0.32  | 0.59  | 0.65  |

SVR and Gradient Boosting models outperform Random Forest on most metrics.

---
