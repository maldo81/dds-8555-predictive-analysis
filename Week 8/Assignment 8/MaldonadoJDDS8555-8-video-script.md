# DDS-8555 Assignment 8 Video Script

This presentation reviews the signature assignment across three prediction settings.  The main point is that the model choice changed because the prediction problem changed.  Store Sales required time series forecasting, House Prices required regression with structured feature engineering, and San Francisco Crime required multiclass classification.

For Store Sales, I submitted ETS and ARIMA forecasts.  ETS produced the stronger public score in this first pass, which suggests that level and seasonality were captured more effectively by exponential smoothing than by the ARIMA specification used here.  A stronger next version would add holiday and promotion structure where future values are available.

For House Prices, I submitted ridge regression and gradient boosting.  Ridge was useful as a stable regularized benchmark, but gradient boosting performed better because housing prices usually involve nonlinear effects, thresholds, and interactions.  The model workflow included dichotomous variables, interactions, polynomial structure, transformations, subset-oriented shrinkage, and dimension reduction.

For San Francisco Crime, I submitted a decision tree, a random forest, and a linear SVM.  The random forest performed best because it averaged many trees and produced more stable class probabilities.  The single tree was interpretable but weak, and the linear SVM was useful as a margin-based comparison but did not match the random forest log-loss score.

The main limitation is that these are first-pass competition models.  They satisfy the assignment requirements and establish a defensible baseline, but future work should tune each model around the competition metric and add stronger diagnostics for calibration, residual structure, and feature stability.
