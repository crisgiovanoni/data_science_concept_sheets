{| class="wikitable"
! Category
! Method
! Description
! Input
! Return
|-
| Filter Methods
| Correlation Thresholds
| -Use correlation matrix and decide what new features to create
| 1. data frame
2. .corr() (pandas)
3. sns.heatmap
| 1. Heatmap with annotated R
|-
| 
| SelectKBest
| -Removes all but highest scoring features
-Looks for:
a. Score as test statistic
b. P-value
-F-regression or Chi-square
-T-tests tells if a single variable is statistically significant; F-test tells if a group of
variables are jointly significant
| 1. SelectKBest method
2. f_regression method (sklearn.feature_selection)
| 1. Selected features that are significant
|-
| Wrapper Methods
| Backward Elimination
| -Model is built already
-Checks performance of model then iteratively remove the worst performing features one by one until
performance is "acceptable"
-Performance metric is p-value. p-value > 0.05, remove feature
| 1. LRmodel (sm.OLS)
2. X and y
3. Conditional (while loop or,boolean mask) that generates p-value and checks for and removes feature with p-value > 0.05
| 1. Resulting feature/s from condition (usually, column name)
|-
| 
| Recursive Feature Elimination (RFE)
| -Recursively removes attributes then builds model on the remaining attributes
-Yields accuracy metric to rank feature according to importance
| 1. LReg model
2. RFE method
3. X and y
| 1. rfe.ranking_ (ranking of variables based on importance level, 1=important)
2. rfe.support_(support of variables (True/False, keep or discard)
|-
| 
| Forward Selection
| 
| 
| 
|-
| Embedded Methods
| LassoCV
| -Penalizes irrelevant features by making its coefficient=0.
-Weights the coefficient by virtue of relevance
-High α ≈ More non-zero value features
| 1. LReg model
2. LassoCV method (sklearn.linear_model)
| 1. alpha_
2. coef_
|-
| 
| Others:
-Elastic Net
-Ridge Regression
-Regularized Regression
| 
| 
| 
|-
| Linear Dimensionality Reduction
| Principal Component Analysis (PCA)
| -Creates a new feature, aka Principal Component which combines X1 and X2
-Ranked in order of explained variance
-Only takes in normalized dataset
-New Principal Components are not interpretable
| 1. PCA method (sklearn.decomposition)
| 1. n_components_
2. pca_explained_variance_ratio_
|}
