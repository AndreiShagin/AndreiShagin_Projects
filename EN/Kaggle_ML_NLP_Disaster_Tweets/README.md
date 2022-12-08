# Identifying Fake and Real Disaster Tweets
> Kaggle dataset. Based on the history of tweets, train a model that will predict a real tweet about a disaster or a fake.

## Content
* [Target](#Target)
* [Steps](#Steps)
* [Libraries](#Libraries)
* [Final result](#Final-result)
* [Output](#Output)

## Target
**Train the model to identify real tweets and fakes**

## Steps
- tweets are cleared of additional characters, stop words
- carried out lemmatization
- made an analysis of popular words separately for tweets about real disasters and fake ones
- trained 4 models with default parameters and hyperparameter fitting

## Libraries
- Models: CatBoost, LightGBM, LinearRegression, Random Forrest, GridSearchCV was used to select parameters
- matplotlib, sklearn, torch, nltk, CountVectorizer, TfidfVectorizer, pymystem3


## Final result
| Model | Test f1 score |
|----------------------|---------------|
| LGBM_model_grid | 0.743854 |
| LGBM_model | 0.743187 |
| model_catboost_cv | 0.756369 |
| model_catboost | 0.752602 |
| decision tree | 0.692712 |
| DecisionTree_grid | 0.62723 |
| LogicRegression | 0.761194 |
| LogicRegression_grid | 0.768182 |

## Conclusion
The best model on the test set LogicRegression 0.7981
