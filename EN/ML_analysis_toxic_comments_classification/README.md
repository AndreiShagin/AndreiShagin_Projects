# Toxic comment Classification
> The online store plans to add functionality that allows users to post comments. It is necessary to train a model that can identify negative and toxic comments and send them for preliminary moderation

## Content
* [Target](#Target)
* [Steps](#Steps)
* [Libraries](#Libraries)
* [Final result](#Final-result)
* [Output](#Output)

## Target
**Train model to detect negative comments.**

Model selection criteria:
* F1 metric value not less than 0.75

## Steps
- text cleaning using regular expressions, lemmatization with POS tag
- an analysis was made with the identification of the most popular words
- three models were trained and hyperparameters were selected

## Libraries
- Models: CatBoostRegressor, LogisticRegression, DecisionTreeClassifier
- matplotlib, nltk, numpy, pandas, sklearn

## Final result
| Model | F1 |
|:---------------------:|:--------:|
| LogisticRegression | 0.732796 |
| LogisticRegression_tuned | 0.755191 |
| DecisionTreeClassifier | 0.732796 |
| DecisionTreeClassifier_tuned | 0.719108 |
| CatBoostRegressor | 0.761723 |
| CatBoostRegressor_cv | 0.764014 |
| LogisticRegression_test | 0.751835 |
| CatBoostRegressor_cv_test | 0.75678 |


## Conclusion
It is recommended to use the CatBoost model as a tool that will look for toxic comments and send them for moderation.
On the validation set, the CatBoost model showed an F1 result of 0.764, on the test set 0.756.
