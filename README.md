# Predicting the covid test result
Ming Tang, last updated on 2021/5/14

## Abstract
* The goal is to use classification models to predict when a person's covid test results (positive/negative).
* Classification models were used for such Predictions
* A local interactive dashboard was built by using Streamlit
* Questions to be answered
  * Can we reliably predict covid test results based on the symptom?
  * If the prediction is possible, what is the contribution/importance of each individual feature?

## Data
* Dataset from this published [article](https://www.nature.com/articles/s41746-020-00372-6) and corresponding [GitHub](https://github.com/nshomron/covidpred/tree/master/data).
* 1 target: corona_results (positive, negative, other)
* 8 features: age, sex, cough, shortness_of_breath, fever, sore_throat, Headache, contact_with_confirmed
* About 3 million rows: each row is one test (all 3 million rows are used in the data explanatory but only 10,000 rows are used for training the classification models for the sake of computation time)


## Tool/Packages used
* Data exploration: pandas, numpy, matplotlib
* Classification: scikit-learn, XGBoost
* Application: Streamlit, Heruko


## Modeling
* Different models, class imbalance, and bagging/boosting approaches are tested.
* The simple LogisticRgression with a threshold of 0.1 generates balanced results
* Final model:
  * P-threshold, 0.1
  * Accuracy, 0.924
  * Precision, 0.58
  * Recall, 0.64
  * F1, 0.61

## App
* The model has been incorporated into an interactive app by using Streamlit and deployed on Heroku.
* [Click here to check it out](https://classification-app-20210513-v3.herokuapp.com/)

![OnlineApp](/figures/app_screenshot.JPG?raw=true)
