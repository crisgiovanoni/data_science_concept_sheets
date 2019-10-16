<table class="tg">
  <tr>
    <th class="tg-xrp7">Category</th>
    <th class="tg-xrp7">Method</th>
    <th class="tg-xrp7">Description</th>
    <th class="tg-xrp7">Input</th>
    <th class="tg-xrp7">Return</th>
  </tr>
  <tr>
    <td class="tg-hvas">Filter Methods</td>
    <td class="tg-hvas">Correlation Thresholds</td>
    <td class="tg-hvas">-Use correlation matrix and decide what new features to create</td>
    <td class="tg-hvas">1. data frame<br>2. .corr() (pandas)<br>3. sns.heatmap</td>
    <td class="tg-hvas">1. Heatmap with annotated R</td>
  </tr>
  <tr>
    <td class="tg-hvas"></td>
    <td class="tg-hvas">SelectKBest</td>
    <td class="tg-hvas">-Removes all but highest scoring features<br>-Looks for:<br>a. Score as test statistic<br>b. P-value<br>-F-regression or Chi-square<br>-T-tests tells if a single variable is statistically significant; F-test tells if a group of<br>variables are jointly significant</td>
    <td class="tg-hvas">1. SelectKBest method<br>2. f_regression method (sklearn.feature_selection)<br></td>
    <td class="tg-hvas">1. Selected features that are significant</td>
  </tr>
  <tr>
    <td class="tg-hvas">Wrapper Methods</td>
    <td class="tg-hvas">Backward Elimination</td>
    <td class="tg-hvas">-Model is built already<br>-Checks performance of model then iteratively remove the worst performing features one by one until<br>performance is "acceptable"<br>-Performance metric is p-value. p-value &gt; 0.05, remove feature</td>
    <td class="tg-hvas">1. LRmodel (sm.OLS)<br>2. X and y<br>3. Conditional (while loop or,boolean mask) that generates p-value and checks for and removes feature with p-value &gt; 0.05</td>
    <td class="tg-hvas">1. Resulting feature/s from condition (usually, column name)</td>
  </tr>
  <tr>
    <td class="tg-hvas"></td>
    <td class="tg-hvas">Recursive Feature Elimination (RFE)</td>
    <td class="tg-hvas">-Recursively removes attributes then builds model on the remaining attributes<br>-Yields accuracy metric to rank feature according to importance</td>
    <td class="tg-hvas">1. LReg model<br>2. RFE method<br>3. X and y</td>
    <td class="tg-hvas">1. rfe.ranking_ (ranking of variables based on importance level, 1=important)<br>2. rfe.support_(support of variables (True/False, keep or discard)</td>
  </tr>
  <tr>
    <td class="tg-hvas"></td>
    <td class="tg-hvas">Forward Selection</td>
    <td class="tg-hvas"></td>
    <td class="tg-hvas"></td>
    <td class="tg-hvas"></td>
  </tr>
  <tr>
    <td class="tg-hvas">Embedded Methods</td>
    <td class="tg-hvas">LassoCV</td>
    <td class="tg-hvas">-Penalizes irrelevant features by making its coefficient=0.<br>-Weights the coefficient by virtue of relevance<br>-High α ≈ More non-zero value features</td>
    <td class="tg-hvas">1. LReg model<br>2. LassoCV method (sklearn.linear_model)</td>
    <td class="tg-hvas">1. alpha_<br>2. coef_</td>
  </tr>
  <tr>
    <td class="tg-hvas"></td>
    <td class="tg-hvas">Others:<br>-Elastic Net<br>-Ridge Regression<br>-Regularized Regression</td>
    <td class="tg-hvas"></td>
    <td class="tg-hvas"></td>
    <td class="tg-hvas"></td>
  </tr>
  <tr>
    <td class="tg-hvas">Linear Dimensionality Reduction</td>
    <td class="tg-hvas">Principal Component Analysis (PCA)</td>
    <td class="tg-hvas">-Creates a new feature, aka Principal Component which combines X1 and X2<br>-Ranked in order of explained variance<br>-Only takes in normalized dataset<br>-New Principal Components are not interpretable</td>
    <td class="tg-hvas">1. PCA method (sklearn.decomposition)</td>
    <td class="tg-hvas">1. n_components_<br>2. pca_explained_variance_ratio_</td>
  </tr>
</table>
