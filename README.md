# Predictive Maintenance: Regression Model Comparison

This project presents a comparative evaluation of three machine learning regression models—Random Forest, Support Vector Regressor (SVR), and Gradient Boosting Regressor—on a sensor dataset for predictive maintenance. The objective is to predict equipment failure using real-valued sensor inputs and identify the most effective model through extensive cross-validation and learning curve analysis.

## 📁 Dataset

The dataset consists of multivariate sensor readings, with each instance labeled by a continuous target value `fail`, indicating equipment degradation or likelihood of failure.

## 📊 Models Compared

- **Random Forest Regressor**
- **Support Vector Regressor (SVR)**
- **Gradient Boosting Regressor**

All models were fine-tuned using Grid Search and validated using 5-fold cross-validation.

## 📈 Metrics Used

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **Coefficient of Determination (R²)**

## 📌 Key Highlights

- Preprocessing included scaling with `StandardScaler` and dropping missing values.
- Best hyperparameters selected via grid search.
- Visual comparisons via bar charts for MAE, RMSE, and R².
- Learning curves to observe model performance vs training size.
- Residual plots to assess bias and variance.
- Random Forest feature importance for interpretability.

## 🔍 Results Summary

| Model                    | MAE   | RMSE  | R²    |
|--------------------------|-------|-------|-------|
| Random Forest            | 0.32  | 0.61  | 0.63  |
| Support Vector Regressor | 0.34  | 0.58  | 0.66  |
| Gradient Boosting        | 0.32  | 0.59  | 0.65  |

## 📷 Visual Outputs

- Metric-wise performance comparison using bar plots.
- Learning curves per model to examine overfitting or underfitting trends.
- Residual plots to validate prediction reliability.
- Feature importance chart from the Random Forest model.
