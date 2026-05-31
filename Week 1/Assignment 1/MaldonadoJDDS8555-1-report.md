# Evaluating Simple Iris Regression and Classification Baselines

## Executive Summary

Predictive analytics is useful only when model performance is evaluated on data the model did not use for fitting because training performance can overstate how well a model will generalize (James et al., 2023).  This analysis used the Iris data set to compare two constant regression estimators for sepal width and two rule-based classifiers for species type.  The data were split into a stratified 80% training set and a 20% test set so the reported metrics would reflect held-out performance rather than training-set fit.

The better regression estimator was the training-set mean of petal length.  It had a mean error of -0.677, MAPE of 24.19%, MAE of 0.694, and MSE of 0.602.  The second estimator, the training-set mean of sepal length minus petal width, had a mean error of -1.543, MAPE of 52.20%, MAE of 1.543, and MSE of 2.526.  Because error was calculated as actual minus predicted, both estimators overpredicted sepal width, but the second overpredicted much more severely.  MAE, MAPE, and MSE all point to the same practical conclusion, although percentage-based error should be interpreted carefully when actual values can approach zero (Hyndman & Koehler, 2006).

The better classifier was the second quantile rule, which used the 50th and 75th percentiles of training sepal length.  It produced accuracy of 0.60 and macro F1 of 0.58, compared with 0.57 accuracy and 0.53 macro F1 for the first rule.  The class-level results still show weak performance, especially for versicolor, which is why precision, recall, and F1 are more useful than accuracy alone for interpreting uneven multiclass results (Sokolova & Lapalme, 2009).  The better next step would not be another one-variable threshold rule.  For sepal-width prediction, linear regression, regularized regression, or tree-based regression should be compared with cross-validation.  For species classification, multinomial logistic regression, k-nearest neighbors, classification trees, support vector machines, or ensemble methods would be more appropriate because they can use all four Iris measurements.  The engineered ratio feature should also be tested rather than assumed useful, because a feature only improves the model if it adds information that generalizes to held-out data.  The current models are useful as metric interpretation baselines, but they should not be treated as strong predictive models.

## References

Hyndman, R. J., & Koehler, A. B. (2006). Another look at measures of forecast accuracy.  *International Journal of Forecasting, 22*(4), 679-688.  https://doi.org/10.1016/j.ijforecast.2006.03.001

James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023). *An introduction to statistical learning: With applications in Python*.  Springer.  https://doi.org/10.1007/978-3-031-38747-0

Sokolova, M., & Lapalme, G. (2009). A systematic analysis of performance measures for classification tasks.  *Information Processing & Management, 45*(4), 427-437.  https://doi.org/10.1016/j.ipm.2009.03.002
