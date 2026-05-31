# Assignment 8: Build and Evaluate Time Series Models

## Executive Summary

The signature assignment compared forecasting, regression, and classification models across three Kaggle competitions.  For Store Sales, ETS outperformed ARIMA on the public score, which suggests that the level and seasonality structure captured by exponential smoothing was more useful than the simple ARIMA specification.  For House Prices, gradient boosting outperformed ridge regression, which is consistent with nonlinear housing-price relationships.  For San Francisco Crime, the random forest outperformed the single decision tree and linear SVM, showing the value of ensemble probability estimates for multiclass log loss.

## Assumptions and Findings

The Store Sales models were evaluated through forecast plausibility, time-order preservation, and residual logic rather than random train-test splitting.  The House Prices models investigated transformations, categorical indicators, interactions, polynomial structure, subset-oriented shrinkage, and dimension reduction.  The SF Crime models treated time, district, and location as structured predictors, but the results remain limited because crime category prediction is affected by class imbalance and unobserved reporting factors.  The completed Kaggle submissions provide the required external evidence for all three competitions.

## Presentation Plan

The PowerPoint and video script summarize the same analytical arc: what each competition asked for, which models were built, how assumptions were checked, which Kaggle submissions completed, and what model family performed best.  The video should emphasize that the goal was not to force one model family across all tasks, but to match method assumptions to each prediction problem.

## References

Breiman, L. (2001). Random forests. *Machine Learning, 45*, 5-32. https://doi.org/10.1023/A:1010933404324
Hyndman, R. J., & Athanasopoulos, G. (2021). *Forecasting: Principles and Practice* (3rd ed.). OTexts. https://otexts.com/fpp3/
Tibshirani, R. (1996). Regression shrinkage and selection via the lasso. *Journal of the Royal Statistical Society: Series B, 58*(1), 267-288. https://doi.org/10.1111/j.2517-6161.1996.tb02080.x