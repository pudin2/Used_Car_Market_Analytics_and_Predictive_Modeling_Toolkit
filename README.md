# Used Car Market Analytics and Predictive Modeling Toolkit

## Overview

This repository contains a set of Jupyter notebooks for exploratory analysis and predictive modeling over a used car market dataset. The project combines descriptive analytics, price prediction, regularized regression, polynomial modeling, and classification techniques to study the drivers of used car prices and vehicle transmission type.

The notebooks are designed as complementary analyses over the same base dataset, progressing from data understanding and preprocessing to regression modeling, model comparison, hyperparameter tuning, and decision tree interpretation.

## Main objectives

- Explore the structure and quality of a used car market dataset.
- Understand the distribution of relevant categorical and numerical vehicle attributes.
- Predict used car selling prices using linear, polynomial, ridge, and lasso regression models.
- Classify vehicle transmission type using decision tree models.
- Compare model behavior across different predictive approaches.
- Interpret model structure and assess trade-offs between predictive power and explainability.

## Repository contents

### Notebooks

- `Used_Car_Market_Exploratory_Analysis.ipynb`  
  Exploratory analysis of the used car dataset, including frequency inspection of categorical variables such as fuel type and ownership structure.

- `Used_Car_Price_Prediction_with_Linear_Regression.ipynb`  
  Baseline linear regression model for predicting selling price after preprocessing numeric and categorical features.

- `Used_Car_Price_Prediction_with_Univariate_Polynomial_Regression.ipynb`  
  Univariate polynomial regression focused on the relationship between `max_power` and `selling_price`, including degree-2 and degree-3 comparisons.

- `Used_Car_Price_Prediction_with_Multivariate_Polynomial_Regression.ipynb`  
  Multivariate polynomial regression model using transformed numerical and dummy-encoded categorical predictors for price prediction.

- `Used_Car_Price_Prediction_with_Ridge_Regression.ipynb`  
  Ridge regression workflow with scaling, validation splits, and hyperparameter tuning using GridSearchCV.

- `Used_Car_Price_Prediction_with_Lasso_Regression.ipynb`  
  Lasso regression workflow with scaling and hyperparameter tuning for sparse regularized price modeling.

- `Used_Car_Price_Prediction_with_Decision_Tree_Tuning_and_Evaluation.ipynb`  
  Decision tree classification pipeline for predicting transmission type, including confusion matrix analysis, precision, recall, F1-score, class balancing, and hyperparameter tuning.

- `Used_Car_Price_Prediction_with_Decision_Tree_Interpretation.ipynb`  
  Interpretation-oriented decision tree notebook with tree visualization and feature-based branching analysis.

### Data files

- `car_details_v3.csv` -> source dataset for all analyses
- `ModeloRegresion.joblib` -> serialized trained regression model
- `decistion_tree.png` -> exported decision tree visualization

## Analytical scope

### 1. Exploratory market analysis

- Frequency analysis of fuel types
- Ownership category distribution
- Basic categorical summaries
- Initial understanding of the used car market structure

### 2. Data preprocessing and feature engineering

- Missing value removal
- Duplicate handling
- Numeric extraction from mixed-format columns such as `mileage`, `engine`, and `max_power`
- Dummy encoding for categorical variables such as `fuel`, `owner`, and `seller_type`
- Label encoding for transmission in classification tasks

### 3. Used car price prediction

- Baseline linear regression
- Univariate polynomial regression
- Multivariate polynomial regression
- Ridge regression with regularization
- Lasso regression with regularization
- Performance comparison using MSE, RMSE, MAE, and R²

### 4. Transmission classification

- Decision tree classification
- Class imbalance inspection
- Accuracy, precision, recall, and F1 evaluation
- Confusion matrix analysis
- Hyperparameter tuning with GridSearchCV
- Model interpretation through tree visualization

## Dataset themes inferred from the notebooks

The analysis uses fields such as:

- `name`
- `year`
- `selling_price`
- `km_driven`
- `fuel`
- `seller_type`
- `transmission`
- `owner`
- `mileage`
- `engine`
- `max_power`
- `torque`
- `seats`

## Modeling highlights

Based on the notebooks currently included in this repository:

- Linear regression provides a solid baseline for selling price prediction.
- Multivariate polynomial regression improves predictive performance over the linear baseline.
- Ridge and Lasso regression introduce regularization for more controlled modeling.
- Decision tree classification achieves strong performance for transmission prediction while remaining interpretable.
- Tree visualization helps explain which features most strongly influence classification splits, especially variables such as `max_power`, `year`, `selling_price`, `engine`, and `mileage`.

## Suggested project structure

Used_Car_Market_Analytics_and_Predictive_Modeling_Toolkit/
│
├── data/
│   └── car_details_v3.csv
│
├── models/
│   └── ModeloRegresion.joblib
│
├── images/
│   └── decistion_tree.png
│
├── notebooks/
│   ├── Used_Car_Market_Exploratory_Analysis.ipynb
│   ├── Used_Car_Price_Prediction_with_Linear_Regression.ipynb
│   ├── Used_Car_Price_Prediction_with_Univariate_Polynomial_Regression.ipynb
│   ├── Used_Car_Price_Prediction_with_Multivariate_Polynomial_Regression.ipynb
│   ├── Used_Car_Price_Prediction_with_Ridge_Regression.ipynb
│   ├── Used_Car_Price_Prediction_with_Lasso_Regression.ipynb
│   ├── Used_Car_Price_Prediction_with_Decision_Tree_Tuning_and_Evaluation.ipynb
│   └── Used_Car_Price_Prediction_with_Decision_Tree_Interpretation.ipynb
│
└── README.md

## Potential business value

This project can support:

- Used car pricing analysis
- Feature importance discovery for resale value
- Vehicle inventory segmentation
- Screening rules for automatic pricing pipelines
- Explainable classification of car transmission profiles
- Benchmarking multiple modeling strategies on the same automotive dataset
