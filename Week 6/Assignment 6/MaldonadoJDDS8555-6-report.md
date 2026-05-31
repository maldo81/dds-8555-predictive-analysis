# Assignment 6: Build and Evaluate Tree Models

## Executive Summary

This assignment used tree-based methods to evaluate how model flexibility changes classification performance.  The conceptual exercise showed how recursive binary splitting partitions feature space into terminal regions.  The applied and Kaggle work used the Obesity data to compare a single decision tree, bagging, random forest, and gradient boosting.

## Model Interpretation

The strongest result came from boosted trees, while the single tree was useful mainly as an interpretable baseline.  Bagging and random forests improved stability by aggregating many trees, and boosting improved accuracy by sequentially reducing residual classification errors.  Assumptions were investigated through validation accuracy, overfitting behavior, and the suitability of tree methods for mixed numeric and categorical predictors.

## References

Breiman, L. (1996). Bagging predictors. *Machine Learning, 24*, 123-140. https://doi.org/10.1007/BF00058655
Breiman, L. (2001). Random forests. *Machine Learning, 45*, 5-32. https://doi.org/10.1023/A:1010933404324
Friedman, J. H. (2001). Greedy function approximation: A gradient boosting machine. *The Annals of Statistics, 29*(5), 1189-1232. https://doi.org/10.1214/aos/1013203451