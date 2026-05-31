# Assignment 7: Build and Evaluate Unsupervised Learning Models

## Executive Summary

This assignment used PCA and clustering to find structure without a labeled outcome.  The conceptual K-means question showed why the algorithm reduces the within-cluster objective at each step.  The USArrests exercise showed that scaling materially changes hierarchical clustering because distance is unit-sensitive.

## Model Interpretation

For the Wine data, PCA reduced correlated chemical variables into enough components to preserve at least 80% of the variance.  K-means was evaluated across multiple values of k using inertia and silhouette scores, while hierarchical clustering provided a second clustering structure.  The results should be treated as exploratory groups, not verified classes, because unsupervised learning identifies structure rather than ground-truth labels.

## References

Jolliffe, I. T. (2002). *Principal component analysis* (2nd ed.). Springer. https://doi.org/10.1007/b98835
MacQueen, J. (1967). Some methods for classification and analysis of multivariate observations. In *Proceedings of the Fifth Berkeley Symposium on Mathematical Statistics and Probability* (Vol. 1, pp. 281-297).
Ward, J. H. (1963). Hierarchical grouping to optimize an objective function. *Journal of the American Statistical Association, 58*(301), 236-244. https://doi.org/10.1080/01621459.1963.10500845