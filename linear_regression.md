<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-top-width:1px;border-bottom-width:1px;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-top-width:1px;border-bottom-width:1px;border-color:black;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-0pky">Category</th>
    <th class="tg-0pky">Method</th>
    <th class="tg-0pky">Description</th>
    <th class="tg-0pky">Input</th>
    <th class="tg-0pky">Return</th>
  </tr>
  <tr>
    <td class="tg-0pky">Filter Methods</td>
    <td class="tg-0pky">Correlation Thresholds</td>
    <td class="tg-0pky">-Use correlation matrix and decide what new features to create</td>
    <td class="tg-0pky">1. data frame<br>2. .corr() (pandas)<br>3. sns.heatmap</td>
    <td class="tg-0pky">1. Heatmap with annotated R</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">SelectKBest</td>
    <td class="tg-0pky">-Removes all but highest scoring features<br>-Looks for:<br>a. Score as test statistic<br>b. P-value<br>-F-regression or Chi-square<br>-T-tests tells if a single variable is statistically significant; F-test tells if a group of<br>variables are jointly significant</td>
    <td class="tg-0pky">1. SelectKBest method<br>2. f_regression method (sklearn.feature_selection)<br></td>
    <td class="tg-0pky">1. Selected features that are significant</td>
  </tr>
  <tr>
    <td class="tg-0pky">Wrapper Methods</td>
    <td class="tg-0pky">Backward Elimination</td>
    <td class="tg-0pky">-Model is built already<br>-Checks performance of model then iteratively remove the worst performing features one by one until<br>performance is "acceptable"<br>-Performance metric is p-value. p-value &gt; 0.05, remove feature</td>
    <td class="tg-0pky">1. LRmodel (sm.OLS)<br>2. X and y<br>3. Conditional (while loop or,boolean mask) that generates p-value and checks for and removes feature with p-value &gt; 0.05</td>
    <td class="tg-0pky">1. Resulting feature/s from condition (usually, column name)</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Recursive Feature Elimination (RFE)</td>
    <td class="tg-0pky">-Recursively removes attributes then builds model on the remaining attributes<br>-Yields accuracy metric to rank feature according to importance</td>
    <td class="tg-0pky">1. LReg model<br>2. RFE method<br>3. X and y</td>
    <td class="tg-0pky">1. rfe.ranking_ (ranking of variables based on importance level, 1=important)<br>2. rfe.support_(support of variables (True/False, keep or discard)</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Forward Selection</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Embedded Methods</td>
    <td class="tg-0pky">LassoCV</td>
    <td class="tg-0pky">-Penalizes irrelevant features by making its coefficient=0.<br>-Weights the coefficient by virtue of relevance<br>-High α ≈ More non-zero value features</td>
    <td class="tg-0pky">1. LReg model<br>2. LassoCV method (sklearn.linear_model)</td>
    <td class="tg-0pky">1. alpha_<br>2. coef_</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Others:<br>-Elastic Net<br>-Ridge Regression<br>-Regularized Regression</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Linear Dimensionality Reduction</td>
    <td class="tg-0pky">Principal Component Analysis (PCA)</td>
    <td class="tg-0pky">-Creates a new feature, aka Principal Component which combines X1 and X2<br>-Ranked in order of explained variance<br>-Only takes in normalized dataset<br>-New Principal Components are not interpretable</td>
    <td class="tg-0pky">1. PCA method (sklearn.decomposition)</td>
    <td class="tg-0pky">1. n_components_<br>2. pca_explained_variance_ratio_</td>
  </tr>
</table>
