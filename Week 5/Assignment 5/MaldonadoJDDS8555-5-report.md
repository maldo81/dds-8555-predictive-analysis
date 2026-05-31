# Assignment 5: Build and Evaluate Classification Models

## Executive Summary

This assignment compared classification methods with different assumptions.  The Weekly exercise showed that a model can produce acceptable overall accuracy while still making asymmetric classification mistakes.  For the Obesity competition, the multinomial logistic and SVM models were stronger than naive Bayes because the input variables are related rather than conditionally independent.

## Model Interpretation

The completed Kaggle submissions include multinomial logistic regression, LDA, naive Bayes, and SVM.  The SVM result was strong because margin-based classifiers can work well when a transformed feature space separates classes more cleanly than the raw variables do (Cortes & Vapnik, 1995).  The notebook documents code, assumptions, validation results, and successful submission evidence.

## References

Cortes, C., & Vapnik, V. (1995). Support-vector networks. *Machine Learning, 20*, 273-297. https://doi.org/10.1007/BF00994018
James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023). *An introduction to statistical learning: With applications in Python*. Springer. https://doi.org/10.1007/978-3-031-38747-0
Sokolova, M., & Lapalme, G. (2009). A systematic analysis of performance measures for classification tasks. *Information Processing & Management, 45*(4), 427-437. https://doi.org/10.1016/j.ipm.2009.03.002