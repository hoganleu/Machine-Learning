# Heart Disease Prediction using Machine Learning Models

This project aims to predict heart disease using two datasets (`heart.csv` and `heart.dat`) and multiple machine learning models. The models include Random Forest (Baseline and Hyperparameter Tuning), Multilayer Perceptron (MLP), and Support Vector Machine (SVM).

---

## Table of Contents
- [Introduction](#introduction)
- [Dataset Setup](#dataset-setup)
- [Models and Evaluation](#models-and-evaluation)
- [Results Summary](#results-summary)
- [Future Work](#future-work)
- [How to Run the Code](#how-to-run-the-code)

---

## Introduction

Heart disease prediction is critical for early diagnosis and treatment. This project explores the effectiveness of different machine learning models on two datasets of varying quality and size. The goal is to evaluate model performance and identify the most suitable approaches.

---

## Dataset Setup

1. Download the datasets:
  Kaggle Heart Disease Dataset - [`heart.csv`](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
  UCI Statlog Heart Dataset - [`heart.dat`](https://archive.ics.uci.edu/dataset/145/statlog+heart)
   
2. Place the datasets in your Google Drive in the following structure:

Google Drive/ └── ML_Project/ ├── heart.csv └── heart.dat
---

## Models and Evaluation

The following machine learning models were implemented and evaluated:

1. **Baseline Models (Random Forest)**
- Baseline models provide a starting point for performance comparison.
- Evaluated on both datasets (`heart.csv` and `heart.dat`).

2. **Hyperparameter Tuning**
- RandomizedSearchCV and GridSearchCV were used to optimize Random Forest parameters.

3. **Multilayer Perceptron (MLP)**
- A simple deep learning model trained and evaluated on both datasets.

4. **Support Vector Machine (SVM)**
- SVM with an RBF kernel was trained and evaluated on standardized datasets.

---

## Results Summary

| Model                     | Dataset    | Accuracy | Precision | Recall | F1-Score | Observations |
|---------------------------|------------|----------|-----------|--------|----------|--------------|
| **Baseline (RF)**         | heart.csv  | 98.54%   | ~99%      | ~99%   | ~99%     | Exceptional performance, indicating high data quality and minimal class imbalance. |
| **Baseline (RF)**         | heart.dat  | 79.63%   | ~79%      | ~79%   | ~79%     | Moderate performance, affected by smaller dataset and class imbalance. |
| **Hyperparameter Tuning** | heart.csv  | 98.54%   | ~99%      | ~99%   | ~99%     | No significant improvement due to already high baseline accuracy. |
| **Hyperparameter Tuning** | heart.dat  | 83.33%   | ~83%      | ~83%   | ~83%     | Moderate improvement achieved with parameter optimization. |
| **MLP**                   | heart.csv  | 98.54%   | 0.99      | 0.99   | 0.99     | High accuracy, suitable for well-processed and balanced datasets. |
| **MLP**                   | heart.dat  | 61.11%   | 0.31      | 0.50   | 0.38     | Poor performance on imbalanced and smaller datasets; struggles with minority class recall. |
| **SVM**                   | heart.csv  | 88.78%   | 0.89      | 0.89   | 0.89     | Balanced performance, slightly lower than MLP, showcasing SVM's robustness on standardized data. |
| **SVM**                   | heart.dat  | 88.89%   | 0.89      | 0.87   | 0.88     | Better performance than MLP on imbalanced datasets; still limited in minority class recall. |

---

## Future Work

- **Dataset Improvements**:
- Implement data augmentation techniques like SMOTE.
- Increase dataset size by acquiring additional data sources.

- **Model Enhancements**:
- Explore advanced algorithms such as Gradient Boosting, XGBoost, or ensemble methods.
- Investigate transfer learning for smaller datasets like `heart.dat`.

- **Pipeline Refinement**:
- Conduct detailed cross-validation experiments for robust performance validation.
- Automate hyperparameter tuning for optimal performance.

---

## How to Run the Code

1. **Install Required Libraries**:
- Ensure the following Python libraries are installed:
  ```bash
  pip install numpy pandas scikit-learn
  ```

2. **Set Up Datasets**:
- Download the datasets from the links provided above.
- Place the datasets in your Google Drive under the following structure:
  ```
  Google Drive/
  └── ML_Project/
      ├── heart.csv
      └── heart.dat
  ```

3. **Run the Python Script**:
- Use the provided script to train and evaluate the models:
  ```bash
  python ml_heart_disease_project.py
  ```

---



