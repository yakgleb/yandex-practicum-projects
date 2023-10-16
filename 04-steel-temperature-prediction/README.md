# Прогноз температуры стали во время плавки

## Описание проекта
Для оптимизации производственных расходов, металлургический комбинат ООО «Так закаляем сталь» решил уменьшить потребление электроэнергии на этапе обработки стали. Нам предстоит построить модель, которая предскажет температуру стали.

## Задачи проекта
Прогнозирование температуры стали во время плавки, решается задача регрессии.

## Навыки и инструменты
Pandas, Sklearn, Seaborn, Matplotlib, Pipeline, GridSearchCV, Numpy, Ridge, XGBoost, SGD, DummyRegressor, Catboost.

## Выводы
В ходе проделанной работы мы:
- провели предобработку и анализ данных (удалили аномалии, обработали пропуски);
- построили различные гистограммы и диаграммы размаха, их детальных анализ помог найти нам различные закономерности;
- создали новые признаки (полная мощность, время плавки стали);
- построим столбчатую диаграмму важности признаков, удалили те признаки, которые оказались бесполезными;
- изучили корреляцию между полученными признаками и удалили признаки, обладающие высокой корреляцией;
- выделили целевой признак и разбили наши данные на тренировочную и тестовую выборку в соотношении 3:1;
- обучили несколько моделей и нашли лучшую из них, ей оказалась модель Catboost при следующих гиперпараметрах: learning_rate = 0.1, depth = 6, n_estimators=100;
- MAE на тестовой выборке для лучшей модели составил 6.5983, при этом MAE для константной модели 7.6230. Мы добились необходимого результата по MAE < 6.8.