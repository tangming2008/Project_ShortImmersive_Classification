# Classification project MVP

Last updated on 2021/5/11 by Ming Tang

**Topic: Predicting covid test results**

## Summary
* Finished
  * data acquisition
  * data exploration
  * 1st round feature engineering,
  * model fitting (tested with KNN, LR, tree, forest, and XGBoost)
  * 1st round model tuning (used GridSearch)
  * preliminary interpretation (feature importance)
* In progress:
  * visualization: will work on streamlit soon (this will be the priority for me)
  * model tuning (will revise parameters in the GridSearchCV)
  * script summary
  * presentation slides

<br>

## Key results so far

## Feature importance
* Figure below shows the feature importance with 95% confidence interval: this is based on the logistical regression, the confidence interval is calculated by the bootstrap approach (with 10000 bags and 10000 samples in each bag)
* “contact_with_confirmed” stands out as the most critical feature for a positive test result.

![Feature importance](/2021.5.11_mvp/figures/1.jpg?raw=true)

## Threshold tuning
* Figure below shows the effect of the decision threshold on the metrics (LogisticRgression model here)
* The key objective of building this model is to maximize the **recall** (i.e. to minimize the false negative / covid-infected people predicted as good). However, the score vs threshold curve (below) clearly show that recall > 0.8 can be only achieved at the significant cost of a lower accuracy. A few advanced ensemble methods (bagging-RandomForest, and boosting-XGboost) have been tested but cannot help increase the recall without compromising the accuracy.
* The limited model performance is likely due to the asymptomatic and non-contacted cases (for all observations: baseline positive rate is about 10%; for all people without any symptoms or “contact_with_confirmed”, the positive rate is still as high as 3.7%)

![Threshold tuning](/2021.5.11_mvp/figures/2.jpg?raw=true)
