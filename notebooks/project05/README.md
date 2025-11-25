# Project 5: Ensemble Machine Learning – Wine Dataset

**Author:** Moses Koroma  
**Course:** Applied Machine Learning  
**Date:** November 2025

## Overview

This project explores ensemble machine learning methods using the Wine Quality Dataset from the UCI Machine Learning Repository. The analysis compares multiple ensemble techniques to predict wine quality categories based on physicochemical properties.

## Dataset

- **Source:** UCI Machine Learning Repository - Wine Quality Dataset
- **File:** `winequality-red.csv`
- **Samples:** 1,599 red wine samples
- **Features:** 11 physicochemical properties (acidity, sugar, alcohol, etc.)
- **Target:** Wine quality scores converted to 3 categories (low, medium, high)

## Models Implemented

### 1. Random Forest (100 trees)
- **Test Accuracy:** 88.75%
- **F1 Score:** 86.61%
- **Overfitting Gap:** 11.3% (moderate overfitting)

### 2. Voting Classifier (DT + SVM + NN)
- **Test Accuracy:** 86.56%
- **F1 Score:** 84.34%
- **Overfitting Gap:** 5.5% (excellent generalization)

## Key Findings

- **Random Forest** achieved the highest accuracy (88.75%) but showed moderate overfitting
- **Voting Classifier** demonstrated better generalization with minimal overfitting
- Both models performed well for wine quality prediction with 86-89% accuracy
- Clear trade-off between peak performance and generalization ability

## Files

- `ml05_moses.ipynb` - Complete analysis notebook with ensemble implementations
- `winequality-red.csv` - Wine Quality dataset (1,599 samples)
- `README.md` - This documentation file

## Requirements

```python
pandas
numpy
matplotlib
scikit-learn
```

## Usage

1. Open `ml05_moses.ipynb` in Jupyter/VS Code
2. Run cells sequentially to reproduce the analysis
3. Dataset is included in the same directory

## Results Summary

The Random Forest model is recommended for maximum accuracy (88.75%), while the Voting Classifier offers better generalization for production use. Both demonstrate the effectiveness of ensemble methods for wine quality prediction based on chemical composition.
