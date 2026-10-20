# Optimizing Maintenance: Evaluating Predictive Accuracy in ML Models for Early Fault Detection[cite: 1, 2]

This repository implements a machine learning framework for predictive maintenance, shifting industrial operations from reactive/preventive methods to proactive condition monitoring within Industry 4.0[cite: 3, 11].

## 📂 Project Overview
This project is part of a Master of Science (M.Sc.) in Data Science thesis[cite: 2]. It evaluates supervised machine learning algorithms to detect early equipment faults and predict machinery failures using industrial sensor telemetry[cite: 3].

## 📊 Dataset
- **Source:** AI4I 2020 Predictive Maintenance Dataset (10,000 operational records)[cite: 24, 34].
- **Target Variable:** Binary classification for `Machine Failure` ($0 = \text{No Failure}$, $1 = \text{Failure}$)[cite: 34].
- **Data Preprocessing & Balancing:** Addressed severe class imbalance using the **Synthetic Minority Over-sampling Technique (SMOTE)**[cite: 3, 26].

## 🛠️ Models Implemented
1. **Logistic Regression:** Parametric linear baseline model[cite: 14].
2. **Random Forest:** Ensemble bagging algorithm using uncorrelated decision trees[cite: 15].
3. **XGBoost:** Regularized gradient-boosting framework optimized for tabular sensor data[cite: 15].

## 📈 Results & Performance
Ensemble methods significantly outperformed the linear baseline model:
- **Random Forest:** **99.1%** Accuracy, **0.99** F1-Score[cite: 38]
- **XGBoost:** **98.95%** Accuracy, **0.99** F1-Score[cite: 39]
- **Logistic Regression:** **82.1%** Accuracy, **0.82** F1-Score[cite: 36]

## 🔍 Feature Importance Analysis
Feature importance evaluation identified the primary operational parameters influencing machinery failure[cite: 52]:
1. **Tool Wear [min]** (Most critical mechanical degradation proxy)[cite: 14, 52]
2. **Torque [Nm]**[cite: 52]
3. **Rotational Speed [rpm]**[cite: 52]
4. **Process Temperature [K]**[cite: 52]
5. **Air Temperature [K]**[cite: 52]

## 🚀 Conclusion
Tree-based ensemble models deliver high predictive accuracy and robustness for structured industrial telemetry without heavy deep learning overhead[cite: 31, 51]. Continuous tracking of tool wear, torque, and rotational speed enables proactive maintenance, minimizing unexpected downtime and operating costs[cite: 16, 52].
