# Проект Классификация комментариев
> Интернет магазин планирует добавить функционал, позволяющий пользователям оставлять комменатрии. Необходимо обучить модель, которая сможет выявлять негативные и токсичные комментарии и отправлять их на предварительную модерацию

## Содержание
* [Цель](#Цель)
* [Последовательность действий](#Последовательность-действий)
* [Использованные библиотеки](#Использованные-библиотеки)
* [Итоговый результат](#Итоговый-результат)
* [Вывод](#Вывод)

## Цель
**Обучить модель для выяления негативных комментариев.**

Критерии выбора модели: 
* значение метрики F1 не менее 0.75

## Последовательность действий
- проведена очистка текста с помощью регулярных выражений, лемматизация с POS tag 
- выполнен анализ с обределеним самых популярных слов 
- обучены три модели и выполнен подбор гиперпараметров

## Использованные библиотеки
- Модели: CatBoostRegressor, LogisticRegression, DecisionTreeClassifier
- matplotlib, nltk, numpy, pandas, sklearn

## Итоговый результат
|            Модель            |    F1    |
|:----------------------------:|:--------:|
| LogisticRegression           | 0.732796 |
| LogisticRegression_tuned     | 0.755191 |
| DecisionTreeClassifier       | 0.732796 |
| DecisionTreeClassifier_tuned | 0.719108 |
| CatBoostRegressor            | 0.761723 |
| CatBoostRegressor_cv         | 0.764014 |
| LogisticRegression_test      | 0.751835 |
| CatBoostRegressor_cv_test    |  0.75678 |


## Вывод
В качестве инструмента, который будет искать токсичные комментарии и отправлять их на модерацию рекомендуется использовать модель CatBoost.
На валидационной выборке модель CatBoost показаала резульата F1 0.764, на тестовой выборке 0.756.
