# Wine Quality Prediction Project

## Overview
In this project, the physicochemical properties of wines are used to predict wine quality and to analyze which features contribute to a wine being classified as "good". Multiple machine learning models were built to evaluate the predictability of wine quality, and feature importance analysis was performed to interpret the results.

## Dataset
The dataset consists of 1599 observations and 12 variables. All physicochemical features are numerical, while the target variable (quality) is an ordinal integer.

## Problem Definition
The original multi-class target variable (wine quality score) was transformed into a binary classification problem:
- Wines with a quality score ≥ 6.5 are labeled as "good"
- Others are labeled as "not good"

This transformation was applied to simplify analysis and improve interpretability.

## Data Analysis
- Outliers were mainly observed in `residual sugar` and `chlorides`, while other features had relatively low outlier ratios.
- Outliers were detected but not removed to avoid data loss.

## Correlation Analysis
- Alcohol showed a positive correlation with wine quality.
- Volatile acidity and total sulfur dioxide showed negative correlations with quality.

## Models Used
- Logistic Regression
- Random Forest
- Gradient Boosting

## Results
- All models achieved strong and similar AUC performance, showing that wine quality is predictable using physicochemical features.
- Tree-based models showed higher recall, making them better at identifying "good" wines.
- Lower recall values were related to class imbalance and default decision thresholds.

## Feature Importance Insights
- Alcohol is the most important predictor of wine quality.
- Sulphates have a positive impact on quality.
- High volatile acidity, chlorides, and sulfur dioxide negatively affect quality.
- Feature importance patterns were consistent across models.

## Conclusion
Machine learning models demonstrate that wine quality can be effectively predicted using physicochemical properties. Alcohol content is the strongest indicator of quality, while acidity and sulfur-related variables negatively influence classification.

## Tools & Technologies
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
