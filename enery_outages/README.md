# Модель машинного обучения, предсказывающая отключения электроэнергии на линиях электропередачи

**Описание проекта:** Обеспечение надежного электроснабжения потребителей при условии поставки им качественной электрической энергии является необходимым условием эффективного развития народного хозяйства. Завышенная протяжённость, совместно с износом сетей приводит к тому, что поток отказов в них доходит до 37 год-1 на 100 км, а время восстановления – до 8 ч. Ущербы от недоотпуска электроэнергии составляют от 30 до 300 руб./кВт·ч и более. Влияет протяжённость и состояние сети и на безопасность эксплуатации. С учётом указанных выше и других проблем в электроснабжении сельских потребителей актуальными являются вопросы поиска способов прогнозирования мест, наиболее подверженных к перерывам в электроснабжении.  

**Данные:** В наличии имеются данные по отключениям электроэнергии в региональных электрических сетях Орловской области за 2018 по 2021 гг. Также имееются данные по характеристикам линий электропередачи (ЛЭП).

**Цель** - разработать модель машинного обучения для прогнозирования возможных отключений электроэнергии на линиях электропередачи на основе характеристик самих ЛЭП.

**Задачи:**

- Подготовка данных к обработке;
- Исследование и обработка данных;
- Удаление и создание признаков;
- Корреляционный анализ;
- Разбиение датасета на обучающую и тестовую выборки;
- Кодирование и масштабирование признаков, при необходимости работа с дисбалансом классов;
- Выбор и обучение разных моделей машинного обучения на кросс-валидации;
- Выбор лучшей модели по метрике ROC-AUC на кросс-валидации;
- Оценка качества лучшей модели на тестовой выборке;
- Изучение важности признаков моделей;
- Выводы.

#### Выводы по проекту:
Для поставленной задачи были обучены следующие модели машинного обучения: LogisticRegression, RandomForestClassifier, LightGBM Classifier, CatBoostClassifier. Наилучшей моделью оказалась  CatBoostClassifier, которая позволяет прогнозировать возможные отключения электроэнергии на линиях электропередачи (110 кВ) на основе характеристик самих ЛЭП со значением метрики ROC-AUC в 0.79.   Наибольшее влияние на прогнозирование моделей ожидаемо составил признак "Протяженность воздушных участков" (66 % для CatBoostClassifier, коэффициент для LogisticRegression - 0,84), так как известно, что чем больше длина ЛЭП, тем больше внешних факторов, способных на ЛЭП оказывать влияние. Большое влияние на прогнозирование моделей оказывает отнесение высоковольтных линий к транзитным ЛЭП или нет (6% и 5%, соответственно, для CatBoostClassifier), при этом, если ЛЭП транзитная, то вероятность ожидания отключений электроэнергии резко возрастает, если не транзитная - то наоборот. Эта особенность хорошо видна на модели логистической регрессии - (коэффициенты равны 0,5 и -0,6 соответственно). Также влияние на прогноз оказывают количество ЖБ опор и протяженность по лесу (лесные массивы вызывают большую вероятность отключений, например, перекрытие проводов ветвями деревьев)..

#
# A machine learning model able to predict power outages on power lines

**Description of the project:** Ensuring reliable power supply to consumers subject to the supply of high-quality electrical energy is a necessary condition for the effective development of national economy. The excessive length together with the wear and tear of power networks lead to the fact that the failure rate of networks reaches 37 year-1 per 100 km, and power resoration time is up to 8 hours. Damages from undersupply of electricity range from 30 to 300 rubles/kWh and more. The length and condition of the network also affects the operation safety. Taking into account the above and other problems in consumers' power supply, the issues of finding ways to predict the places most susceptible to power supply outages are relevant.

**Data:** Data on power outages in regional electric networks of the Oryol region for 2018 to 2021 are available. There is also data on the characteristics of power transmission lines (PTL).

**The goal** is to develop a machine learning model able to predict possible power outages on power lines based on the characteristics of PTLs.

**Tasks**:

- Data preparation;
- Data analysis and data processing;
- Features removing and creation;
- Correlation analysis;
- Splitting the dataset into training and test samples;
- Coding and scaling of features, if necessary, working with class imbalance;
- Selection and training of different ML models for cross-validation;
- Selecting the best model based on the ROC-AUC metric for cross-validation;
- Assessing best model quality on test sample;
- Analysis of feature importance for models;
- Conclusions.

#### Project Conclusions:
For the task, such ML models as LogisticRegression, RandomForestClassifier, LightGBM Classifier, CatBoostClassifier were trained. The best model turned out to be CatBoostClassifier, which allows predicting possible power outages on power lines (110 kV) based on the characteristics of the power lines themselves with a ROC-AUC metric value of 0.79. The greatest influence on model forecasting is made by the feature “Length of air sections” (66% for CatBoostClassifier, coefficient for LogisticRegression - 0.84), since it is known that the greater the length of the power line is, the more external factors that can influence the power line are. The classification of high-voltage lines as transit power lines or not (6% and 5%, respectively, for CatBoostClassifier) has a great influence on the models' forecast. The probability of expecting power outages increases sharply if  a power line is transit If it is not transit, then vice versa. This feature is clearly visible by the logistic regression model - coefficients are 0.5 and -0.6, respectively. The forecast is also influenced by the number of reinforced concrete supports and the length of the forest zones (forests cause a higher probability of outages, for example, the crossing of wires by tree branches).
