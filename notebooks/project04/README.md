# Project 4 – Regression Modeling with Titanic Dataset

**Author:** Moses Koroma  
**Course:** Applied Machine Learning  
**Date:** November 2025

## Project Overview

This project demonstrates regression modeling techniques using the famous Titanic dataset. Instead of the typical classification approach (predicting survival), this analysis focuses on **predicting passenger fares** as a continuous target variable.

## Objectives

- Apply various regression techniques to predict ticket fares
- Compare model performance across different complexity levels
- Analyze the impact of feature engineering and regularization
- Evaluate overfitting in polynomial models
- Provide comprehensive model comparison and insights

## Project Structure

```
project04/
├── ml04_moses.ipynb    # Main analysis notebook
├── README.md           # This file
└── data/
    └── titanic/
        ├── train.csv   # Training dataset (located in ../../data/titanic/)
        ├── test.csv    # Test dataset
        └── gender_submission.csv
```

## Analysis Sections

### 1. Data Loading & Inspection
- Load Titanic dataset
- Explore data structure and column types
- Identify missing values and data quality issues

### 2. Data Preparation & Feature Engineering
- Handle missing values in Age and Fare columns
- Encode categorical variables (Sex)
- Create new features (FamilySize)
- Data preprocessing for modeling

### 3. Model Development

#### **Case 1: Linear Regression (Age → Fare)**
- Simple linear regression using only passenger age
- Baseline model performance

#### **Case 2: Linear Regression (Age + Pclass → Fare)**
- Multiple linear regression with age and passenger class
- Feature combination analysis

#### **Case 3: Polynomial Regression**
- **Degree 3**: Moderate complexity polynomial features
- **Degree 8**: High complexity polynomial features
- Overfitting analysis

#### **Case 4: Regularized Models**
- **Ridge Regression**: L2 regularization on degree 8 polynomials
- **ElasticNet**: Combined L1/L2 regularization
- Regularization effectiveness evaluation

### 4. Model Comparison & Summary
- Comprehensive performance metrics table
- Visual comparisons across all models
- Best model identification

### 5. Final Reflection
- Analytical questions and evidence-based answers
- Feature importance analysis
- Overfitting detection and regularization impact

## Models Implemented

| Model Type | Features | Complexity | Regularization |
|------------|----------|------------|----------------|
| Linear Regression | Age | Low | None |
| Linear Regression | Age + Pclass | Low | None |
| Polynomial (deg=3) | Age | Medium | None |
| Polynomial (deg=8) | Age | High | None |
| Ridge Regression | Age (deg=8) | High | L2 |
| ElasticNet | Age (deg=8) | High | L1 + L2 |

## Evaluation Metrics

All models are evaluated using:
- **Mean Absolute Error (MAE)**: Average absolute prediction error
- **Root Mean Square Error (RMSE)**: Square root of average squared errors
- **Mean Squared Error (MSE)**: Average squared prediction error
- **R² Score**: Coefficient of determination (explained variance)

## Technologies Used

- **Python 3.x**
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib**: Data visualization
- **scikit-learn**: Machine learning algorithms and metrics
  - `LinearRegression`, `Ridge`, `ElasticNet`
  - `PolynomialFeatures`
  - `train_test_split`
  - Evaluation metrics

## Getting Started

1. **Prerequisites:**
   ```bash
   pip install pandas numpy matplotlib scikit-learn
   ```

2. **Data Setup:**
   - Ensure Titanic dataset is located at `../../data/titanic/train.csv`
   - Or update the data path in the notebook accordingly

3. **Run Analysis:**
   - Open `ml04_moses.ipynb` in Jupyter Notebook or VS Code
   - Execute cells sequentially
   - Review results and visualizations

## Key Findings

### Feature Performance
- **Age + Passenger Class** significantly outperformed Age alone
- Passenger class is a strong predictor of fare prices
- Feature combinations capture more underlying relationships

### Model Performance
- Best performing model: [Model name with highest R²]
- Optimal balance of accuracy and generalization

### Overfitting Analysis
- Higher-degree polynomials showed [evidence of overfitting/good generalization]
- Regularization [was/was not] effective in controlling overfitting

### Regularization Impact
- Ridge and ElasticNet [improved/maintained/degraded] performance
- Optimal regularization strategy identified

**Moses Koroma**  
Applied Machine Learning Course  
November 2025
