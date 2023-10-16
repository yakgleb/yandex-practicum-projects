# Построение модели определения стоимости автомобиля

## Описание проекта
Сервис по продаже автомобилей с пробегом  разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. На основе исторические данные необходимо построить модель для определения стоимости автомобиля.

## Задачи проекта
Разработка системы рекомендации стоимости автомобиля на основе его описания, решается задача регрессии.

## Навыки и инструменты
Sklearn, Pandas, Catboost, Pipeline, OneHotEncoder, StandardScaler, LightGBM, DecisionTreeRegressor, GridSearchCV

## Выводы
Мы выполнили предобработку данных, удалив дубликаты, пропуски и выбросы, а также проработали нулевые значения. Потом мы отбросили ненужные признаки (которые не нужны для обучения моделей), затем преобразовали категориальные признаки в численные. После чего разибили данные на обучающую и валидационную выборки и провели обучение трех моделей: LightGBM, Дерево решений и CatBoostRegressor с помощью перебора гиперпараметров через Pipeline.

Определили лучшую модель и проверили ее на тестовой выборке, ей оказалась CatBoostRegressor, метрика RMSE на тестовой выборке вышла 1647.99 (должна быть <2500 по условию).