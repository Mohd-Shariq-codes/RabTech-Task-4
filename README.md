# Titanic Survival Prediction — Model Comparison & Tuning

A supervised machine learning project developed as part of the RabTech Academy Internship Task 4. The project focuses on training, evaluating, and comparing multiple classification algorithms to predict passenger survival on the Titanic dataset.

## Project Overview

The objective of this project is to build and compare multiple machine learning classification models, perform model evaluation, and identify the best-performing model using appropriate performance metrics.

The project includes model training, performance comparison, hyperparameter tuning, and champion model selection.

## Objectives

- Train at least four different machine learning classification models.
- Perform hyperparameter optimization.
- Apply cross-validation for reliable model evaluation.
- Evaluate models using standard classification metrics.
- Compare model performance using a structured comparison table.
- Select the best-performing model as the Champion Model.
- Save the model for future predictions.

## Machine Learning Models

The following classification algorithms were evaluated:

1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. Support Vector Machine (SVM)

## Model Comparison Results

The following results are taken from `model_comparison.csv`.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 81.56% | 77.27% | 73.91% | 75.56% | 85.13% |
| Random Forest | 79.89% | 75.38% | 71.01% | 73.13% | 84.39% |
| Gradient Boosting | 79.89% | 78.95% | 65.22% | 71.43% | 79.92% |
| SVM | 79.89% | 75.38% | 71.01% | 73.13% | 82.83% |

## Key Findings

- **Best Accuracy:** Logistic Regression — 81.56%
- **Best Precision:** Gradient Boosting — 78.95%
- **Best Recall:** Logistic Regression — 73.91%
- **Best F1-Score:** Logistic Regression — 75.56%
- **Best ROC-AUC:** Logistic Regression — 85.13%

## Champion Model

**Selected Model: Logistic Regression**

Based on the supplied model comparison results, Logistic Regression achieved the highest Accuracy, Recall, F1-Score, and ROC-AUC among the evaluated models.

Its ROC-AUC score of 85.13% indicates good ability to distinguish between the two target classes.

Gradient Boosting achieved the highest Precision at 78.95%.

Logistic Regression is therefore the current champion based on the overall comparison. Final selection should also consider the validation strategy and the project's chosen optimization metric.

## Evaluation Metrics

The models were compared using the following metrics:

- **Accuracy:** Measures the proportion of correct predictions.
- **Precision:** Measures the proportion of positive predictions that are correct.
- **Recall:** Measures how many actual positive cases are correctly identified.
- **F1-Score:** Combines Precision and Recall using their harmonic mean.
- **ROC-AUC:** Measures the model's ability to distinguish between the two classes across different classification thresholds.

Additional evaluation artifacts include confusion matrices and ROC curves where implemented in the notebook.

## Project Workflow

1. Load the Titanic dataset.
2. Prepare the input features and target variable.
3. Handle missing values and encode categorical features as required.
4. Split the dataset into training and testing sets.
5. Train four classification algorithms.
6. Perform hyperparameter tuning using GridSearchCV or Optuna, as implemented.
7. Apply Stratified K-Fold Cross-Validation where configured.
8. Evaluate the models using classification metrics.
9. Generate a model comparison table and ROC-AUC curves.
10. Select the Champion Model.
11. Save the selected model in `.pkl` or `.joblib` format.
12. Store the comparison results in `model_comparison.csv`.

## Project Structure

```text
RabTech-Task-4/
│
├── data/
│   └── dataset files
│
├── notebooks/
│   └── task4_modeling.ipynb
│
├── models/
│   └── champion_model.joblib
│
├── model_comparison.csv
├── requirements.txt
└── README.md
