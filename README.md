# Machine Learning for Infrastructure Reliability & Power Grid Outage Prediction

This repository delivers an end-to-end predictive maintenance framework designed to analyze historical data, detect anomalies, and forecast power supply outages across **110 kV overhead power lines**. 

By leveraging gradient-boosted architectures, this system identifies high-risk grid sectors, allowing utility providers to optimize field maintenance schedules, reduce system downtime, and prevent substantial operational losses.

---

### 📊 Applied R&D Project Framework & Source Code

| Module & Jupyter Architecture | Engineering & Data Science Objective | Core Tech Stack |
| :--- | :--- | :---: |
| 🔍 **[Part 1: Exploratory Data Analysis & Feature Processing](https://github.com/VadZhen/Agro_and_energy_science_projects/blob/main/enery_outages/outages_MLmodel_1_Colab.ipynb)** | Handled extreme data sparsity, missing environmental vectors, and conducted feature engineering based on power transmission line (PTL) structural characteristics, age, and topological exposure. | **Python, Pandas, NumPy, Matplotlib, Seaborn** |
| 🤖 **[Part 2: Predictive ML Modeling & Hyperparameter Tuning](https://github.com/VadZhen/Agro_and_energy_science_projects/blob/main/enery_outages/outages_MLmodel_2_Colab.ipynb)** | Engineered binary classification models trained on historical fault records. Managed heavy class imbalance, conducted rigorous validation strategies, and executed hyperparameter optimization using advanced gradient boosting to achieve a stable **ROC-AUC of 0.78**. | **Python, LightGBM, CatBoost, Scikit-Learn, SciPy** |

---

### ⚙️ Engineering & Data Science Workflow

1. **Data Ingestion & Integrity:** Aggregated heterogenous datasets containing power grid technical logs, structural asset details, and geographical statistics.
2. **Feature Engineering:** Synthesized complex asset-health indicators (wear-and-tear coefficients, fault rate risk scaling, and structural exposure variables).
3. **Statistical Pruning:** Executed collinearity matrices and feature importance rankings to eliminate redundant architectural signals and prevent overfitting.
4. **Model Architecture Optimization:** Benchmarked linear classifiers against `LightGBM` and `CatBoost` boosting frameworks under stratified cross-validation pipelines to eliminate data leakage.

---

### 🔬 Peer-Reviewed International Publication

The core methodology, data preprocessing pipelines, and machine learning models implemented in this repository have been fully validated, peer-reviewed, and published in the international open-access journal **Energies** (2025):

* **Paper Title:** *Power Outage Prediction on Overhead Power Lines on the Basis of Their Technical Parameters: Machine Learning Approach*
* **Citation:** Bolshev, V.; Budnikov, D.; Dzeikalo, A.; Korolev, R. *Energies* 2025, 18(18), 5034.
* **Official Link:** [https://doi.org/10.3390/en18185034](https://doi.org/10.3390/en18185034)

---

### 🏆 Key Technical Achievements
* **Predictive Performance:** Reached an operational **ROC-AUC of 0.78** on heavily imbalanced, real-world utility asset data.
* **Production Methodology:** Designed via encapsulated Python structures ensuring reproducibility and strict separation between feature processing and model training phases.
* **Global Validation:** Backed by high-impact international R&D indexing, establishing a solid baseline for real-world predictive maintenance applications.

---
*Note: This repository represents core R&D implementations conducted during my tenure as a Senior Scientist specializing in system reliability and advanced data modeling.*
