# Machine Learning for Infrastructure Reliability & Power Grid Outage Prediction

This repository delivers an end-to-end predictive maintenance framework designed to analyze historical data, detect anomalies, and forecast power supply outages across **110 kV overhead power lines**. 

By leveraging gradient-boosted architectures, this system identifies high-risk grid sectors, allowing utility providers to optimize field maintenance schedules, reduce system downtime, and prevent substantial operational losses.

---

### 📊 Applied R&D Project Framework

| System Framework & Source Code | Core Research & Engineering Objective | Technical Stack | Research & Publication Status |
| :--- | :--- | :---: | :--- |
| 🔍 **[Part 1: Exploratory Data Analysis & Feature Processing](https://github.com/VadZhen/Agro_and_energy_science_projects/blob/main/enery_outages/outages_MLmodel_1_Colab.ipynb)** | Handled extreme data sparsity, missing environmental vectors, and conducted feature engineering based on power transmission line (PTL) structural characteristics, age, and topological exposure. | **Python, Pandas, NumPy, Matplotlib, Seaborn** | **Peer-Reviewed & Published:** <br/> 📄 [Research Paper 1: Data Analytics & EDA Framework](http://journal.sfu-kras.ru/article/153857) |
| 🤖 **[Part 2: Predictive ML Modeling & Hyperparameter Tuning](https://github.com/VadZhen/Agro_and_energy_science_projects/blob/main/enery_outages/outages_MLmodel_2_Colab.ipynb)** | Engineered binary classification models trained on historical fault records. Managed heavy class imbalance, conducted rigorous validation strategies, and executed hyperparameter optimization using advanced gradient boosting to achieve a stable **ROC-AUC of 0.78**. | **Python, LightGBM, CatBoost, Scikit-Learn, SciPy** | **Peer-Reviewed & Published:** <br/> 📄 [Research Paper 2: Predictive Modeling & Optimization](http://journal.sfu-kras.ru/article/154403) |

---

### ⚙️ Engineering & Data Science Workflow

1. **Data Ingestion & Integrity:** Aggregated heterogenous datasets containing power grid technical logs, structural asset details, and geographical statistics.
2. **Feature Engineering:** Synthesized complex asset-health indicators (wear-and-tear coefficients, segment length risk scaling, and line capacity exposure).
3. **Statistical Pruning:** Executed collinearity matrices and feature importance rankings to eliminate redundant architectural signals and prevent overfitting.
4. **Model Architecture Optimization:** Benchmarked linear classifiers against `LightGBM` and `CatBoost` boosting frameworks under stratified cross-validation.
5. **Business-Driven Interpretability:** Extracted global feature importance to isolate the dominant technical factors driving system degradation, providing actionable data for utility engineering teams.

---

### 🏆 Key Technical Achievements
* **Predictive Performance:** Reached a highly operational **ROC-AUC of 0.78** on heavily imbalanced, real-world utility data.
* **Production Deployment Ready:** Modeled via clean, modular Python pipelines ensuring reproducibility and preventing data leakage between data preparation and training stages.
* **Validated Science:** The algorithms, feature selections, and statistical conclusions are fully backed by two peer-reviewed scientific publications in leading engineering journals.

---
*Note: This repository represents core R&D implementations conducted during my tenure as a Senior Scientist specializing in system reliability and advanced data modeling.*
