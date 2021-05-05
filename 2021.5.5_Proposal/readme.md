# Classification project proposal

Last updated on 2021/5/5 by Ming Tang


**Topic: Predicting covid test results**


Questions to be answered
* Can we reliably predict covid test results based on the symptom?
* If the prediction is possible, what is the contribution/importance of each features?


Data to be used
* Dataset from this published [article](https://www.nature.com/articles/s41746-020-00372-6) and corresponding [GitHub blog](https://github.com/nshomron/covidpred/tree/master/data).
* 1 target: Covid test result (positive, negative, other)
* 8 features: Age, Sex, Cough, Shortness of breath, Fever, Sore_throat, Headache, Contact_with_confirmed
* About 3 million rows: each row is one test


Future planning
1. Review and explore the dataset (by May 7)
2. Get extra datasets if needed, such as geographic data (by May 7)
3. Perform the classification prediction and model tuning (KNN, Logistic, Decision tree, by May 10)
4. Review the classification metrics on the model performance (by May 10)
4. Explore the opportunity of hosting the preliminary model result online (like the [Cleveland Clinic](https://riskcalc.org/COVID19/); potential tool: Streamlit)


Additional notes
* Due to the limited feature numbers, I will explore more in the contribution/importance of the feature on the prediction probability. For example, is covid infection more sensitive to cough or fever?
* Minimum viable product (MVP): a model with multiple classification algorithms tested
* I appreciate great notes and comments from the instructors (Joan and Kim) and TAs (Tawney and Ethan)
