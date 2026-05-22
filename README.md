# ⚙️ Predictive Maintenance Model

> Predicting machine failures before they happen — trained on sensor data from 10,000 machines using multi-class classification.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

## 📌 Project Overview

Unplanned machine downtime is one of the most costly problems in manufacturing. This project builds a **predictive maintenance system** that uses operational sensor data to classify the type of failure a machine is likely to experience — before it actually fails.

Trained and evaluated **4 machine learning classifiers** on a dataset of 10,000 machines, selecting the best-performing model for deployment-ready recommendation.

---

## 📊 Dataset

| Property | Details |
|---|---|
| Machines | 10,000 |
| Features | Temperature, power output, torque, tool wear rate, rotational speed |
| Target | 5 failure types (multi-class classification) |
| Class Balance | Handled via analysis during EDA |

### Failure Types
| Label | Failure Type |
|---|---|
| 0 | No Failure |
| 1 | Heat Dissipation Failure |
| 2 | Power Failure |
| 3 | Overstrain Failure |
| 4 | Tool Wear Failure |
| 5 | Random Failure |

---

## 🔍 Methodology

1. **Data Ingestion & Cleaning** — Handled missing values, outliers, and data type corrections using Pandas
2. **Exploratory Data Analysis (EDA)** — Visualised feature distributions, class imbalance, and correlations
3. **Feature Engineering** — Derived meaningful features from raw sensor readings; applied label encoding for multi-class targets
4. **Model Training** — Trained 4 classifiers with consistent train/test splits
5. **Model Evaluation** — Compared models on accuracy, precision, recall, and F1-score
6. **Feature Importance** — Identified top predictors using Random Forest feature importance scores

---

## 📈 Model Comparison

| Model | Test Accuracy |
|---|---|
| 🥇 Random Forest | **98.5%** |
| 🥈 Logistic Regression | 98.05% |
| 🥉 Decision Tree | 97.70% |
| SVM | 96.15% |

> ✅ **Random Forest selected as the final model** based on highest test accuracy and robustness to overfitting.

---

## 🔑 Key Findings

- **Overstrain and Heat Dissipation** were identified as the strongest failure predictors via feature importance analysis
- Random Forest outperformed all other classifiers across all evaluation metrics
- Feature engineering from raw sensor readings (temperature, torque, tool wear rate) significantly improved model performance

---

## 💡 Business Impact

- Enables maintenance teams to **act before failure occurs**, reducing unplanned downtime
- Classifying failure *type* (not just yes/no) allows targeted interventions — e.g. cooling fixes for heat dissipation vs. load reduction for overstrain
- A 98.5% accurate model on 10,000 machines translates to significant cost savings in a real manufacturing environment

---

## 🛠️ Tech Stack

- **Python** — Core development language
- **Pandas / NumPy** — Data cleaning and feature engineering
- **Scikit-learn** — Model training, evaluation, and comparison
- **Matplotlib / Seaborn** — EDA visualisations and feature importance plots
- **Jupyter Notebook** — Development and documentation

---

## 📁 Repository Structure

```
predictive-maintenance/
│
├── data/
│   └── predictive_maintenance.csv     # Raw sensor dataset
│
├── notebooks/
│   └── predictive_maintenance.ipynb   # Full analysis and modelling notebook
│
├── outputs/
│   ├── model_comparison.png           # Accuracy comparison chart
│   └── feature_importance.png         # Top predictors plot
│
├── requirements.txt
└── README.md
```

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/HeatxCliff/predictive-maintenance.git
cd predictive-maintenance

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook notebooks/predictive_maintenance.ipynb
```

---

## 📦 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

---

## 👤 Author

**Kartik Divte**
📧 kartikdivte@gmail.com
💼 [LinkedIn](https://www.linkedin.com/in/kartikdivte/)
