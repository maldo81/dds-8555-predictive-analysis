# Assignment 3: Build Non-Linear Models Part 1

## Executive Summary

This assignment treated model selection as a balance between predictive accuracy and stability.  Best subset selection has the lowest training RSS for a fixed model size because it searches the full model space, but that does not guarantee the lowest test RSS.  The simulated polynomial exercise showed the same point in practice: selection methods can recover real signal, but they can also include extra terms when the sample is noisy.

## Model Interpretation

For the Abalone competition, elastic net regression gave a stronger and more interpretable regularized baseline than the PCR ridge model.  PCR reduced the predictor space, but it also moved the interpretation from original variables to components.  The completed Kaggle submissions document both required models, while the notebook keeps the code and validation results visible.

## References

Hastie, T., Tibshirani, R., & Friedman, J. (2009). *The elements of statistical learning: Data mining, inference, and prediction* (2nd ed.). Springer. https://doi.org/10.1007/978-0-387-84858-7
Jolliffe, I. T. (2002). *Principal component analysis* (2nd ed.). Springer. https://doi.org/10.1007/b98835
Tibshirani, R. (1996). Regression shrinkage and selection via the lasso. *Journal of the Royal Statistical Society: Series B, 58*(1), 267-288. https://doi.org/10.1111/j.2517-6161.1996.tb02080.x