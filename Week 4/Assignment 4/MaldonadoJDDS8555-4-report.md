# Assignment 4: Build Non-Linear Models Part 2

## Executive Summary

This assignment moved beyond straight-line regression by evaluating nonlinear feature behavior in the Auto data and nonlinear tree-based models in the Abalone competition.  The conceptual basis-function question showed how a knot changes the slope and curvature of a fitted function.  In the applied work, polynomial terms improved the Auto model, which supports the practical need for flexible model forms.

## Model Interpretation

For the Abalone submissions, gradient boosting and random forest both satisfied the nonlinear modeling requirement.  Gradient boosting performed best on Kaggle, which is consistent with its ability to build a sequence of weak learners that focus on remaining error (Friedman, 2001).  The result supports using nonlinear methods when the relationship is structured but not well represented by a single global line.

## References

Friedman, J. H. (2001). Greedy function approximation: A gradient boosting machine. *The Annals of Statistics, 29*(5), 1189-1232. https://doi.org/10.1214/aos/1013203451
Hastie, T., & Tibshirani, R. (1990). *Generalized additive models*. Chapman and Hall.
James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023). *An introduction to statistical learning: With applications in Python*. Springer. https://doi.org/10.1007/978-3-031-38747-0