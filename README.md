# Heart Disease Prediction with Machine Learning

## Overview
This project aims to predict heart disease using two datasets: `heart.csv` and `heart.dat`. Machine learning techniques, particularly Random Forest classifiers, were employed to analyze these datasets. The project focuses on baseline model performance, hyperparameter tuning, and feature importance analysis to improve prediction accuracy.

## Datasets
- **heart.csv**: A well-balanced dataset with sufficient data size. It achieved high accuracy in predictions due to well-represented features.
- **heart.dat**: A smaller dataset with moderate accuracy, likely impacted by data size and class imbalance.

## Key Results
- **heart.csv**:
  - Baseline Accuracy: **98.54%**
  - Optimized Accuracy: **98.54%** (No significant improvement due to already high baseline accuracy)
- **heart.dat**:
  - Baseline Accuracy: **79.63%**
  - Optimized Accuracy: **83.33%** (Achieved through hyperparameter tuning)

## Feature Importance
The following visualizations show the feature importance for both datasets:

### Feature Importance - heart.csv Dataset
![Feature Importance - heart.csv](heart_csv_feature_importance.png)

### Feature Importance - heart.dat Dataset
![Feature Importance - heart.dat](heart_dat_feature_importance.png)

## Methodology
1. **Data Preprocessing**:
   - One-hot encoding for categorical variables.
   - Standardization of features.
   - Train-test split with an 80-20 ratio.
2. **Baseline Models**:
   - Random Forest Classifiers were trained on both datasets to establish baseline performance.
3. **Hyperparameter Tuning**:
   - Techniques like `GridSearchCV` and `RandomizedSearchCV` were used to optimize the Random Forest models.
4. **Evaluation Metrics**:
   - Accuracy, Precision, Recall, and F1-Score were used to assess model performance.

## Detailed Report
For a detailed explanation of the methodology, results, and analysis, refer to the [CVPR-Formatted Report](Heart_Disease_Prediction_Report.pdf).

## Getting Started
To reproduce the results, follow these steps:
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/heart-disease-prediction.git
