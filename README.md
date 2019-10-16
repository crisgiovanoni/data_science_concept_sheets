<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
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
    <td class="tg-0pky">Filter Method</td>
    <td class="tg-0pky">Correlation Thresholds</td>
    <td class="tg-0pky">-Use correlation matrix and decide what new features to create</td>
    <td class="tg-0pky">1. data frame<br>2. .corr() (pandas)<br>3. sns.heatmap</td>
    <td class="tg-0pky">1. Heatmap with annotated R</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">1. SelectKBest method<br>2. f_regression method (sklearn.feature_selection)<br></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">SelectKBest</td>
    <td class="tg-0pky">-Removes all but highest scoring features</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">1. Selected features that are significant</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Looks for:</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Score as test statistic</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">P-value</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-F-regression or Chi-square</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-T-tests tells if a single variable is statistically significant; F-test tells if a group of variables are jointly significant</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Wrapper Method</td>
    <td class="tg-0pky">Backward Elimination</td>
    <td class="tg-0pky">-Model is built already</td>
    <td class="tg-0pky">1. LRmodel (xsm.OLS)<br>2. X and y<br>3. Conditional (while loop or boolean mask) that generates p-value and checks for and removes feature with p-value &gt; 0.05</td>
    <td class="tg-0pky">1. resulting feature/s from condition (usually, column name)</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Checks performance of model then iteratively remove the worst performing features one by one until performance is "acceptable"</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Performance metric is p-value. p-value &gt; 0.05, remove feature</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Recursive Feature Elimination (RFE)</td>
    <td class="tg-0pky">-Recursively removes attributes then builds model on the remaining attributes</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">1. rfe.ranking_ (ranking of variables based on importance level, 1=important)</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Accuracy metric to rank feature according to importance</td>
    <td class="tg-0pky">2. RFE method</td>
    <td class="tg-0pky">2. rfe.support_(support of variable (True/False, keep or discard)</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">3. X and y</td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Embedded Methods</td>
    <td class="tg-0pky">LassoCV</td>
    <td class="tg-0pky">-Penalizes irrelevant features by making its coefficient=0.</td>
    <td class="tg-0pky">1. LReg model</td>
    <td class="tg-0pky">1. alpha_</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Weights the coefficient by virtue of relevance</td>
    <td class="tg-0pky">2. LassoCV method (sklearn.linear_model)</td>
    <td class="tg-0pky">2. coef_</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-High α, More non-zero value features</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Others:&nbsp;&nbsp;Elastic Net, Ridge Regression, Regularized Regression</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Linear Dimensionality Reduction</td>
    <td class="tg-0pky">Principal Component Analysis (PCA)</td>
    <td class="tg-0pky">-Creates a new feature, aka Principal Component which combines X1 and X2</td>
    <td class="tg-0pky">1. PCA method (sklearn.decomposition)</td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Ranked in order of explained variance</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-Only takes in normalized dataset</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">-New Principal Components are not interpretable.</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
</table>
