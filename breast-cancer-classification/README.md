# Breast Cancer Classification Using Machine Learning

## Project Overview

This project develops and evaluates machine learning models for classifying breast tumors as **malignant or benign** using the Breast Cancer Wisconsin dataset available through scikit-learn.

Three classification algorithms were compared:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

The workflow includes exploratory data analysis, data preprocessing, model development, cross-validation, hyperparameter tuning, final model evaluation, and model interpretation.

## Dataset

The dataset contains:

- **569 observations**
- **30 numerical predictor variables**
- Two diagnosis classes:
  - Malignant
  - Benign

The data were divided into:

- 70% Training
- 15% Validation
- 15% Test

Stratified sampling was used to preserve the class distribution across each subset.

## Machine Learning Workflow

1. Data exploration and visualization
2. Train-validation-test split
3. Feature standardization
4. Logistic Regression
5. Random Forest
6. Support Vector Machine
7. Validation performance comparison
8. Five-fold cross-validation
9. Hyperparameter tuning
10. Final model evaluation
11. Model interpretation

## Model Comparison

| Model | Mean CV Accuracy |
|---|---:|
| Logistic Regression | **97.99%** |
| Random Forest | 97.25% |
| SVM | 96.98% |

Logistic Regression achieved the highest average cross-validation accuracy and demonstrated strong stability across folds.

## Final Model Performance

Logistic Regression was selected as the final model.

| Metric | Test Performance |
|---|---:|
| Accuracy | **98.84%** |
| Malignant Precision | **100.00%** |
| Malignant Recall | **96.88%** |
| Malignant F1-Score | **98.41%** |
| ROC-AUC | **0.995** |

The final model correctly classified **85 of 86 test observations**, including:

- 31 of 32 malignant cases
- 54 of 54 benign cases

## Key Findings

- Logistic Regression provided the strongest balance between predictive performance, stability, simplicity, and interpretability.
- The model achieved excellent discrimination between malignant and benign observations with an ROC-AUC of 0.995.
- Radius-, concavity-, and tumor-size-related measurements were among the important predictors in distinguishing between the two classes.
- Cross-validation showed that more complex models did not provide better generalization than Logistic Regression.

## Tools & Technologies

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Notebook

The complete analysis, including exploratory data analysis, model development, evaluation, and interpretation, is available in:

`breast_cancer_classification.ipynb`

## Disclaimer

This project is intended as a machine learning demonstration and should not be interpreted as a clinically validated diagnostic system.
