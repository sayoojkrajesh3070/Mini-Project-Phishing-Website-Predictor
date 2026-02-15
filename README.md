# Phishing Website Predictor 🛡️

## 🎯 Project Objective
The goal of this project is to build an automated Machine Learning system capable of detecting phishing websites with high precision. By analyzing 49 different URL and webpage features, the model distinguishes between malicious and legitimate links to protect users from credential theft and financial fraud.

## 📂 Dataset Information
- **Name:** Phishing_Legitimate_full.csv
- **Size:** 10,000 samples (Balanced: 5,000 Phishing / 5,000 Legitimate)
- **Features:** 49 structural and statistical features (e.g., URL Length, Number of Dots, Hostname Length, Presence of IP Address).
- **Target:** `CLASS_LABEL` (1 for Phishing, 0 for Legitimate).

## 🛠️ Project Workflow
The project follows a rigorous 17-step roadmap including:
1. **Data Cleaning:** Handled missing values via median imputation and capped outliers using the IQR method.
2. **EDA:** Conducted correlation analysis and visualized feature distributions using Seaborn.
3. **Feature Selection:** Identified the top 15 "heavy hitter" features using Random Forest importance.
4. **Pipeline Construction:** Integrated `StandardScaler` and the classifier into a single Scikit-Learn Pipeline to prevent data leakage.
5. **Hyperparameter Tuning:** Optimized the model using `GridSearchCV`.

## 🤖 Models Applied
We evaluated 5 classification algorithms:
- **Random Forest (Champion Model):** Best at capturing non-linear patterns.
- **Support Vector Machine (SVM):** High-dimensional boundary separation.
- **Logistic Regression:** Baseline linear classification.
- **K-Nearest Neighbors (KNN):** Similarity-based clustering.
- **Naive Bayes:** Probabilistic classification.

## 🏆 Key Results
The **Random Forest Classifier** emerged as the best model.

| Metric | Score |
| :--- | :--- |
| **Accuracy** | 98.2% |
| **F1-Score** | 0.98 |
| **ROC-AUC** | 0.99 |

**Conclusion:** The model is highly reliable with a generalization gap of less than 1%, indicating it is not overfitted and is ready for real-world testing.

## 🚀 Future Work
- **Deep Learning:** Implementing an LSTM (Long Short-Term Memory) network for character-level URL analysis.
- **Real-time API:** Developing a browser extension to flag URLs as users browse.
- **Dynamic Updates:** Periodically retraining the model to recognize "Zero-Day" phishing patterns.

## 👤 Author
- **Name:** Sayooj K Rajesh
- **Organization:** Entri Elevate
- **Date:** February 15, 2026
