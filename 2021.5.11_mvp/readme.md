# Classification project MVP

Last updated on 2021/5/11 by Ming Tang

**Topic: Predicting covid test results**


Summary
* Finished
  * Data acquisition
  * Exploration, 
  * 1st round feature engineering, 
  * model fitting
  * 1st round model tuning (tested KNN, LR, tree, forest, ensemble)
  * preliminary interpretation (feature importance)
* In progress: 
  * visualization: will work on streamlit soon (this will be the priority for me)
  * model tuning (will revise parameters in the GridSearchCV)
  * script summary
  * presentation slides
  
  <br>

**Key results so far**

Figure 1 of feature importance
Feature important with 95% confidence interval: This is based on the logistical regression, the confidence interval is calculated by the bootstrap (with 10000 bags and 10000 samples in each bag)

![Feature importance](/2021.5.11_mvp/figures/1.jpg?raw=true)

Example figure 2 of Threshold tuning
The key objective of building this model is to maximize the **recall** (i.e. to minimize the false negative, covid-infected people predicted as good). However, the score vs threshold curve (below) clearly show that recall > 0.8 can be only achieved at the significant cost of a lower accuracy. A few advanced ensemble methods (bagging-RandomForest, and boosting-XGboost) are tested cannot help increase the recall. The underlying theory behind this is that asymptomatic people (the features are essentially zero and impossible to separate these people out). 

![Threshold tuning](/2021.5.11_mvp/figures/1.jpg?raw=true)
