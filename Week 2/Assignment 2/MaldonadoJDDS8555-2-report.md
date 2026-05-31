# Assignment 2: Build Regression Models

## Executive Summary

This assignment used regression as both an interpretive and predictive tool.  The ISLP salary question showed why interaction terms must be interpreted conditionally rather than as isolated coefficients.  In the Carseats model, Price and the US indicator carried the practical signal, while Urban did not add clear evidence once the other predictors were included.  The smaller fitted model was Sales = 13.031 - 0.0545(Price) + 1.200(US), which supports a directional interpretation but not a complete sales forecast because R2 remained low.  The Abalone competition extended the same logic into prediction: the ridge model provided a regularized linear baseline, while the random forest captured nonlinear structure and produced the stronger Kaggle result.

## Assumptions and Findings

The regression checks focused on linearity, independence of residuals, collinearity, and residual distribution because those assumptions shape how much trust can be placed in coefficient interpretation (Snee, 1977).  For Carseats, Durbin-Watson was close to 2, VIF values were low, Jarque-Bera did not show strong residual non-normality, and the residual plots did not show a severe pattern.  The Kaggle evidence documented two completed Assignment 2 submissions: ridge with public/private scores of 0.16442/0.16372 and random forest with public/private scores of 0.14927/0.14943.  The code is maintained in the GitHub-backed course repository at `https://github.com/maldo81/data-science-phd.git`.  Overall, the work supports using the simpler regression model for explanation and the more flexible model for competition prediction, with the notebook documenting code, validation, submission evidence, and limitations.

## References

Hastie, T., Tibshirani, R., & Friedman, J. (2009). *The elements of statistical learning: Data mining, inference, and prediction* (2nd ed.). Springer. https://doi.org/10.1007/978-0-387-84858-7
James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023). *An introduction to statistical learning: With applications in Python*. Springer. https://doi.org/10.1007/978-3-031-38747-0
Snee, R. D. (1977). Validation of regression models: Methods and examples. *Technometrics, 19*(4), 415-428. https://doi.org/10.1080/00401706.1977.10489581
