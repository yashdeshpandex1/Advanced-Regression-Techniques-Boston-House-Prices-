# Advanced Regression Techniques on Boston Housing Data

This project explores and compares classical linear regression, regularization methods, subset selection, and dimension-reduction techniques to predict median house prices using the Boston Housing dataset.

The objective is to evaluate how different regression families handle multicollinearity, bias–variance trade-offs, and generalization performance using cross-validation.

## 📊 Dataset

The Boston Housing dataset contains socioeconomic and housing-related variables with median home value as the target.

## Features
Feature	Description
CRIM	Per capita crime rate
ZN	Proportion of residential land zoned
INDUS	Proportion of non-retail business acres
CHAS	Charles River dummy variable
NOX	Nitric oxides concentration
RM	Average number of rooms
AGE	Proportion of older homes
DIS	Distance to employment centers
RAD	Accessibility to highways
TAX	Property tax rate
PTRATIO	Pupil–teacher ratio
B	Proportion of Black population
LSTAT	% lower status population
MEDV	Median house value (target)
🧠 Models Implemented

The following regression techniques were implemented and compared:

Multiple Linear Regression

Ridge Regression

Lasso Regression

Forward Stepwise Selection

Principal Component Regression (PCR)

Partial Least Squares (PLS)

These models allow comparison between unregularized, regularized, and dimension-reduction approaches.

## 🛠️ Methodology

Standardized predictors where required (Ridge, Lasso, PCR, PLS).

Used K-Fold Cross-Validation for model tuning and selection.

Evaluated models using:

Cross-validated Mean Squared Error (MSE)

Test-set performance

Analyzed coefficient shrinkage and feature selection behavior.

## 📈 Results
Model	Test / CV MSE
Ridge Regression	20.45
Lasso Regression	20.86
Multiple Linear Regression	20.99
Forward Selection	21.12
PLS Regression	26.99
PCR (PCA)	30.95
🔍 Key Findings

Ridge Regression achieved the lowest MSE, outperforming both unregularized and dimensionality-reduction methods.

Regularization effectively mitigated multicollinearity, especially among correlated predictors such as RAD, TAX, and NOX.

Lasso performed competitively but did not surpass Ridge, indicating that feature shrinkage was more beneficial than feature elimination.

PCR and PLS showed higher error, suggesting that variance-based component selection was less effective than coefficient regularization for this dataset.

## ✅ Conclusion

Regularized regression models, particularly Ridge Regression, provide the best balance between bias and variance for the Boston Housing dataset. This project highlights the importance of cross-validation and model selection when working with correlated predictors in real-world regression problems.
