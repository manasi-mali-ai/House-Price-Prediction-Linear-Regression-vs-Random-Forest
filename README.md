# Boston Housing Price Prediction

This repository contains code and analysis comparing the predictive performance of Linear Regression (LR) and Random Forest (RF) models for predicting housing prices in Boston. The aim is to assess which model provides better accuracy in estimating the median value of owner-occupied homes based on various features.

## Introduction

This report compares the predictive performance of LR and RF models using the Boston Housing Dataset. The goal is to provide insights into the effectiveness of these algorithms for housing price prediction tasks.

## Data Description

The dataset used in this analysis contains various attributes describing housing properties in Boston suburbs. Each data point represents a suburb, with features such as crime rate, proportion of residential lots, and more. The target variable is the median value of owner-occupied homes (MEDV), serving as the indicator of housing prices.

- `crim`: Per capita crime rate by town.
- `zn`: Proportion of large residential lots (over 25,000 sq. ft.).
- `indus`: Proportion of non-retail business acres per town.
- `Chas`: Binary variable indicating if the property is near Charles River (1 for yes, 0 for no).
- `nox`: Concentration of nitrogen oxides in the air.
- `rm`: Average number of rooms per dwelling.
- `age`: Proportion of old owner-occupied units built before 1940.
- `dis`: Weighted distances to Boston employment centres.
- `rad`: Index of accessibility to radial highways.
- `tax`: Property tax rate per $10,000.

## Preprocessing

1. Handling Missing Values: Null rows were dropped as the null percentage was less than 5%.
2. Outlier Detection and Capping: Outliers were identified and replaced with capped values within predefined limits to control their impact on model training.

## Model Training

Both Linear Regression (LR) and Random Forest (RF) models were trained using the scikit-learn library in Python.

## Evaluation Metrics

### Linear Regression:
- MSE (Mean Squared Error): 12.71
- MAE (Mean Absolute Error): 2.71
- R2 (Coefficient of Determination): 0.757
- Cross-Validation MAE: 2.80
- Cross-Validation R2: 0.764

### Random Forest:
- MSE: 7.15
- MAE: 1.94
- R2: 0.863
- Cross-Validation MAE: 2.02
- Cross-Validation R2: 0.857

- MSE and MAE: RF outperforms LR, indicating better accuracy.
- R2: RF explains a larger proportion of the variance in the target variable.
- Cross-Validation Scores: Both models exhibit similar performance, but RF maintains lower MAE and higher R2.

## Conclusion

Based on the results, the Random Forest model appears superior to Linear Regression for predicting housing prices in this dataset. However, further analysis and optimization, such as feature engineering and hyperparameter tuning, could improve both models.
