# Diabetes Risk Prediction in Women

**By: Niharika Dwivedi**

## Overview

This project investigates whether adding age, BMI, and family history as predictors 
improves diabetes risk prediction compared to a single logistic regression model 
using only blood pressure. The analysis is conducted on female patients of Pima 
Indian descent, aged 21 and older.

## Research Question

How does the addition of age, BMI, and family history improve the prediction of 
diabetes risk compared to a single logistic regression model using only blood pressure?

## Dataset

- **Source:** National Institute of Diabetes and Digestive and Kidney Diseases 
  (via Kaggle)
- **Observations:** 768 female patients (268 diabetic, 500 non-diabetic)
- **Population:** Women of Pima Indian descent, aged 21+

### Variables Used

| Variable | Description |
|---|---|
| BloodPressure | Diastolic blood pressure (mmHg) |
| Age | Age in years |
| BMI | Body Mass Index |
| DiabetesPedigreeFunction | Genetic likelihood of diabetes (0–2.5) |
| Outcome | Diabetes diagnosis (1 = Yes, 0 = No) |

## Methods

- Exploratory Data Analysis (scatterplots, boxplots, correlation coefficients)
- Multicollinearity check using Variance Inflation Factor (VIF)
- **Inferential:** Likelihood Ratio Test comparing two nested logistic regression models
- **Predictive:** ROC curve comparison with AUC scores (70/30 train-test split)

## Key Results

| Model | Predictors | AUC |
|---|---|---|
| Simple Model | Blood Pressure only | 0.55 |
| Multiple Model | Blood Pressure + Age + BMI + Family History | 0.74 |

- Age, BMI, and DiabetesPedigreeFunction were each statistically significant (p < 0.05)
- Blood pressure alone was **not** a significant predictor (p = 0.057)
- The likelihood ratio test confirmed the multiple model is a significantly better 
  fit (p ≈ 2.25e-28)

## Technologies Used

- R (tidyverse, ggplot2, caret, pROC, glmnet, car)
- Google Colab

## How to Run

1. Open the notebook in Google Colab
2. Run all cells from top to bottom
3. The dataset is loaded automatically via the Kaggle API

## References

- CDC. (2024). *Diabetes and Men.*
- Chauhan, A. (2022). *Predict Diabetes.* Kaggle.
- Gale, E., & Gillespie, K. (2001). Diabetes and gender. *Diabetologia*, 44, 3–15.
