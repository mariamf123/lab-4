# MSCS_634_Lab_4

# Diabetes Progression Prediction — Regression Models Lab

# mariam Fathima

## Mariam

## 26.03.2026

## Purpose of the Lab Work

This lab investigates how well different regression models can predict diabetes progression
using a dataset sourced from sklearn. The core objective is to compare the performance of
five models — Linear Regression, Multiple Regression, Polynomial Regression, Ridge
Regression, and Lasso Regression — by examining their accuracy, behavior under different
conditions, and susceptibility to overfitting. The dataset consists of various
health-related attributes of diabetic patients, with the target variable representing the
extent of disease progression.

---

## Models Implemented

### Linear Regression

Linear Regression is a foundational model that operates under the assumption that a
straight-line relationship exists between the input features and the output variable. It
can work with either a single feature or multiple features when making predictions.

### Multiple Regression

Multiple Regression builds upon Linear Regression by utilizing several input features
simultaneously to predict the target variable. This approach enables a richer and more
detailed understanding of how different features collectively influence the outcome.

### Polynomial Regression

Polynomial Regression is an extension of Linear Regression that introduces polynomial
terms to account for non-linear patterns in the data. It is particularly well-suited for
situations where the relationship between features and the target variable is too complex
for a simple linear model to capture.

### Ridge Regression

Ridge Regression modifies standard Linear Regression by incorporating L2 regularization,
which discourages overly large coefficient values. This penalty-based approach improves
the model's ability to generalize, particularly in scenarios involving multicollinearity
among features.

### Lasso Regression

Lasso Regression applies L1 regularization to Linear Regression, which serves a dual
purpose — reducing overfitting while simultaneously performing automatic feature selection
by shrinking certain coefficients to exactly zero, retaining only the most informative
predictors.

---

## Model Evaluation and Results

### Linear Regression

| Metric | Value |
| ------ | ----- |
| R²     | 0.233 |
| MAE    | 52.26 |
| RMSE   | 63.73 |

Linear Regression yielded weak results, with its R² score indicating that the model could
only account for 23.3% of the variance in the target variable. The relatively high MAE
and RMSE values further confirm that the model's predictions deviated considerably from
the actual values.

### Multiple Regression

| Metric | Value |
| ------ | ----- |
| R²     | 0.453 |
| MAE    | 42.79 |
| RMSE   | 53.85 |

Multiple Regression offered a notable improvement over its simpler counterpart, explaining
approximately 45% of the target variance. The reduction in both MAE and RMSE reflects a
meaningful gain in predictive accuracy when multiple features are taken into account.

### Polynomial Regression

| Metric | Value |
| ------ | ----- |
| R²     | 0.233 |
| MAE    | 52.18 |
| RMSE   | 63.75 |

Polynomial Regression performed on par with Linear Regression, offering no measurable
gain in predictive performance. The model also exhibited signs of overfitting when
higher-degree polynomials were used, resulting in error values nearly identical to those
of the basic linear model.

### Ridge Regression

| Metric | Value |
| ------ | ----- |
| R²     | 0.419 |
| MAE    | 46.14 |
| RMSE   | 55.47 |

Ridge Regression outperformed both Linear and Polynomial Regression by leveraging L2
regularization to reduce the risk of overfitting. Although it did not rank as the top
model, its regularization mechanism contributed to improved generalization across the
dataset.

### Lasso Regression

| Metric | Value |
| ------ | ----- |
| R²     | 0.472 |
| MAE    | 42.85 |
| RMSE   | 52.90 |

Lasso Regression delivered the strongest results among all models tested, recording the
highest R² and the lowest error values. Its combined capacity for regularization and
feature selection proved effective in minimizing overfitting and maximizing predictive
precision.

---

## Model Comparison Summary

| Model                 | R²    | MAE   | RMSE  |
| --------------------- | ----- | ----- | ----- |
| Linear Regression     | 0.233 | 52.26 | 63.73 |
| Multiple Regression   | 0.453 | 42.79 | 53.85 |
| Polynomial Regression | 0.233 | 52.18 | 63.75 |
| Ridge Regression      | 0.419 | 46.14 | 55.47 |
| Lasso Regression      | 0.472 | 42.85 | 52.90 |

---

## Key Insights

- **Lasso Regression** stood out as the top-performing model, achieving the best scores
  across all evaluation metrics while successfully curbing overfitting through built-in
  feature selection.
- **Multiple Regression** and **Ridge Regression** both offered meaningful improvements
  over the simpler models, benefiting from the use of additional features and
  regularization techniques respectively.
- **Polynomial Regression** posed a risk of overfitting, particularly at higher polynomial
  degrees, and failed to deliver any substantial improvement over basic Linear Regression.
- The results clearly underscore the value of **regularization** — as demonstrated by
  both Ridge and Lasso — in controlling model complexity and promoting better
  generalization.

---

## Conclusion

This lab examined a range of regression approaches applied to the task of predicting
diabetes progression from a clinical dataset. **Lasso Regression** proved to be the most
effective model, combining regularization with feature selection to achieve superior
accuracy and robustness. **Ridge Regression** and **Multiple Regression** also showed
commendable performance compared to their simpler counterparts. Overall, the experiment
reinforces the significance of regularization strategies in building predictive models
that generalize well, avoid overfitting, and deliver reliable results on unseen data.

