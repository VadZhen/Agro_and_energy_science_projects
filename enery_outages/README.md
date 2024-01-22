# Модель машинного обучения, предсказывающая уход клиентов оператора связи

## Проект выполнен в качестве финальной работы на курсе по Data Science  от Yandex Practicum

**Описание проекта:** Оператору связи «Ниединогоразрыва.ком» необходимо предсказывать отток клиентов. Если согласно предсказанию, пользователь планирует уйти, ему должны быть предложены промокоды и специальные условия. Для предсказания требуется разработать качественную модель машинного обучения с метрикой ROC-AUC на тестовой выборке в 0.85. Помимо ROC-AUC необходимо предоставить интерпретируемую метрику, такие как accuracy и матрица ошибок.

**Цель работы** - построить модель машинного обучения, предсказывающая уход клиентов оператора, при чем метрика ROC-AUC на тестовой выборке должна составлять не менее 0.85.

**Выполненные задачи**: 

- Подготовка данных к обработке
- Исследование и обработка данных
- Удаление и создание признаков
- Корреляционный анализ
- Разбиение датасета на обучающую и тестовую выборки
- Кодирование и масштабирование признаков, при необходимости работа с дисбалансом классов
- Выбор и обучение разных моделей машинного обучения на кросс-валидации
- Выбор лучшей модели по метрике ROC-AUC на кросс-валидации
- Оценка качества лучшей модели на тестовой выборке
- Анализ других метрик, построение матрицы ошибок и изучение важности признаков лучшей модели.
- Выводы



#### Выводы по проекту:
Для поставленной задачи были обучены следующие модели машинного обучения: LogisticRegression, RandomForestClassifier, LightGBM Classifier, CatBoostClassifier. Наилучшей моделью оказалась  CatBoostClassifier, которая позволяет прогнозировать возможные отключения электроэнергии на линиях электропередачи (110 кВ) на основе характеристик самих ЛЭП со значением метрики ROC-AUC в 0.79.   Наибольшее влияние на прогнозирование моделей ожидаемо составил признак "Протяженность воздушных участков" (66 % для CatBoostClassifier, коэффициент для LogisticRegression - 0,84), так как известно, что чем больше длина ЛЭП, тем больше внешних факторов, способных на ЛЭП оказывать влияние. Большое влияние на прогнозирование моделей оказывает отнесение высоковольтных линий к транзитным ЛЭП или нет (6% и 5%, соответственно, для CatBoostClassifier), при этом, если ЛЭП транзитная, то вероятность ожидания отключений электроэнергии резко возрастает, если не транзитная - то наоборот. Эта особенность хорошо видна на модели логистической регрессии - (коэффициенты равны 0,5 и -0,6 соответственно). Также влияние на прогноз оказывают количество ЖБ опор и протяженность по лесу (лесные массивы вызывают большую вероятность отключений, например, перекрытие проводов ветвями деревьев)..

#
# A machine learning model able to predict the departure of telecom operator customers

## The project was completed as the final work in the Data Science course from Yandex Practicum

**Description of project:** The telecom operator “Niedinogorazryva.com” needs to predict customers' outflow. According to the prediction, if the user plans to leave, he should be offered promotional codes and special conditions. For prediction, it is necessary to develop a high-quality ML model with a ROC-AUC metric on a test sample of 0.85. In addition to ROC-AUC, interpretable metrics such as accuracy and error matrix should be provided.

**The goal of work** is to build a ML model able to predict the departure of telecom operator customers, and the ROC-AUC metric on the test sample should be at least 0.85.

**Completed tasks**:

- Initial familiarization with the data
- Data merging
- Isolation of the target feature
- Data analysis and processing
- Removing and creating features
- Correlation analysis
- Splitting the dataset into training and test samples
- Feature encoding and scaling
- Selection and training of different machine learning models with cross-validation
- Selecting the best model based on the ROC-AUC metric with cross-validation
- Assessing the quality of the best model on the test sample
- Construction and analysis of the ROC curve, accuracy, error matrix and importance of features for the best model on test sample.
- Progress report

- Preparing data for processing
- Research and data processing
- Removing and creating features
- Correlation analysis
- Splitting the dataset into training and test samples
- Coding and scaling of features, if necessary, working with class imbalance
- Selection and training of different machine learning models for cross-validation
- Selecting the best model based on the ROC-AUC metric for cross-validation
- Assessing the quality of the best model on the test sample
- Analysis of other metrics, construction of an error matrix and study of the importance of features of the best model.
- Conclusions
- 

#### Project Conclusions:
For the task, such ML models as LogisticRegression, RandomForestClassifier, LightGBM Classifier, CatBoostClassifier were trained. The best model turned out to be CatBoostClassifier, which allows predicting possible power outages on power lines (110 kV) based on the characteristics of the power lines themselves with a ROC-AUC metric value of 0.79. The greatest influence on model forecasting is made by the feature “Length of air sections” (66% for CatBoostClassifier, coefficient for LogisticRegression - 0.84), since it is known that the greater the length of the power line is, the more external factors that can influence the power line are. The classification of high-voltage lines as transit power lines or not (6% and 5%, respectively, for CatBoostClassifier) has a great influence on the models' forecast. The probability of expecting power outages increases sharply if  a power line is transit If it is not transit, then vice versa. This feature is clearly visible by the logistic regression model - coefficients are 0.5 and -0.6, respectively. The forecast is also influenced by the number of reinforced concrete supports and the length of the forest zones (forests cause a higher probability of outages, for example, the crossing of wires by tree branches).
