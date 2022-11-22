Ссылка | Направление | Цель | Вывод | Используемые библиотеки
------------- |------------- |---------------- | ---------------- | -----------------------
[Определение фэйковых и реальных твитов про катастрофы](https://github.com/AndreiShagin/AndreiShagin_Projects/blob/main/RU/Kaggle_ML_NLP_Disaster_Tweets/Natural_Language_Processing_with_Disaster_Tweets.ipynb) | Machine learning, NLP | Обучить модель для прогнозирования определения принадлежности твита к фэйку или реальному, целевая метрика F1 | На тренировочной выборке модель LogicRegression показаала резульата F1 0.76, на тестовой выборке 0.79. При выполнении проведена очистка текста с помощью регулярных выражений, лемматизация с POS tag, обучены 4 модели и выполнен подбор гиперпараметров.   | `Pandas`, `NumPy`, `Sklearn`, `CatBoostRegressor`, `NLTK`, `LogisticRegression`, `Matplotlib`, `Seaborn`, `WordNetLemmatizer`, `LightGBM`,`TfidfVectorizer` , `DecisionTree`