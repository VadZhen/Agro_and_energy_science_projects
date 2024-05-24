# Модель машинного обучения, предсказывающая отключения электроэнергии на линиях электропередачи

**Описание проекта:** Обеспечение надежного электроснабжения потребителей при условии поставки им качественной электрической энергии является необходимым условием эффективного развития народного хозяйства. Завышенная протяжённость, совместно с износом сетей приводит к тому, что поток отказов в них доходит до 37 год-1 на 100 км, а время восстановления – до 8 ч. Ущербы от недоотпуска электроэнергии составляют от 30 до 300 руб./кВт·ч и более. Влияет протяжённость и состояние сети и на безопасность эксплуатации. С учётом указанных выше и других проблем в электроснабжении сельских потребителей актуальным является разработка способов поиска мест, наиболее подверженных к перерывам в электроснабжении.  

**Данные:** В наличии имеются данные по отключениям электроэнергии в региональных электрических сетях Орловской области за 2018 по 2023 гг. Также имееются данные по характеристикам линий электропередачи (ЛЭП).

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
Для поставленной задачи были обучены следующие модели машинного обучения: SVM, LogisticRegression, RandomForestClassifier, LightGBM Classifier и CatBoostClassifier. Наилучшей моделью оказалась  LogisticRegression, которая позволяет прогнозировать возможные отключения электроэнергии на линиях электропередачи (110 кВ) на основе характеристик самих ЛЭП со значением метрики ROC-AUC в 0.78.  
Согласно оценке важности признаков, наибольший вклад в прогнозирование моделей вносит признак «Протяженность воздушных участков ЛЭП». Протяженность ЛЭП по населенной местности показывает наличие обратной зависимости с целевой переменной, то есть чем больше протяженность ЛЭП по населенной местности, тем ниже вероятность отказов на ней. В тоже самое время протяженность по лесу имеет довольно слабую корреляцию с фактом отказов. Касательно типов опор, выявлено, что большее содержание ЖБ опор относительно металлических опор влечет за собой повышение вероятности отказов на ЛЭП. Сильное влияние на вероятность отключений на ЛЭП 110 кВ дает факт транзитности линии. Срок эксплуатации и состояния ЛЭП оказывают довольно слабое влияние на целевую переменную.

#
# A machine learning model able to predict power outages on power lines

**Description of the project:** Ensuring reliable power supply to consumers subject to the supply of high-quality electrical energy is a necessary condition for the effective development of national economy. The excessive length together with the wear and tear of power networks lead to the fact that the failure rate of networks reaches 37 year-1 per 100 km, and power resoration time is up to 8 hours. Damages from undersupply of electricity range from 30 to 300 rubles/kWh and more. The length and condition of the network also affects the operation safety. The length and condition of the network also affects the operation safety. Taking into account the above and other problems in consumers' power supply, it is relevant to develop ways to find places that are most susceptible to power supply outages.


**Data:** Data on power outages in regional electric networks of the Oryol region for 2018 to 2023 are available. There is also data on the characteristics of power transmission lines (PTL).

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
For the task, such ML models as SVM, LogisticRegression, RandomForestClassifier, LightGBM Classifier и CatBoostClassifier were trained. The best model turned out to be LogisticRegression, which allows predicting possible power outages on power lines (110 kV) based on the characteristics of the power lines themselves with a ROC-AUC metric value of 0.78. According to the assessment of the importance of features, the greatest contribution to model forecasting is made by the feature “Length of overhead power line sections”. The length of power lines in a populated area shows the presence of an inverse relationship with the target variable, that is, the greater the length of power lines in a populated area, the lower the probability of failures on it. At the same time, the line length through forest has a rather weak correlation with the fact of failures. Regarding the types of supports, it was found that a higher content of reinforced concrete supports relative to metal supports entails an increase in the likelihood of failures on power lines. The fact that the line is transitive has a strong influence on the probability of outages on 110 kV power lines. The service life and condition of power lines have a rather weak effect on the target variable.
