# Car price prediction
> An online used car sales service needs a machine learning model so that any site visitor can use it to get an estimate of the cost of their car. Main goal: to train the model to determine the market value of used cars.

## Content
* [Target](#Target)
* [Steps](#Steps)
* [Libraries](#Libraries)
* [Final result](#Final-result)
* [Output](#Output)

## Target
**Train the model to determine the market value of used cars.**

Model selection criteria:
* quality - root mean square error (RMSE)
* speed and time of learning/prediction.

## Steps
- pre-processing is done (duplicates, missing values, outliers)
- Models were trained and predicted with default parameters and additionally using different sets of hyperparameters.
- the best model was selected based on the results of the RMSE metric and training time.

## Libraries
- Models: CatBoost, LightGBM, LDecisionTree,LogicRegression
- matplotlib, seaborn, pandas, sklearn

## Final result
| | Training time, sec | Prediction time, sec | RMSE |
|------------:|:--------------------:|:----- --------------------:|:-----------:|
| LightGBM | 0.453220 | 0.096657 | 1619.491135 |
| LightGBM_tune | 1.905599 | 0.096657 | 1528.083352 |
| Linear Regression | 2.531641 | 0.254325 | 2615.396890 |
| Random Forest | 2.531641 | 0.411866 | 1631.064896 |
| RandomForest_tune | 38.452305 | 0.413474 | 1622.971090 |
| catboost | 58.845365 | 0.165132 | 1597.171163 |
| catboost_cv | 64.517677 | 0.259060 | 1569.805924 |

## Conclusion
The best model for learning rate, predictions is LGBM.
Based on this, the general recommendation is:
As a model to use for predicting used car prices, it is recommended to choose LGBM with fitted hyperparameters.
