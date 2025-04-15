# 🧠 Diabetes Prediction Using Ensemble Models

This project builds a high-recall binary classification model to predict diabetes using real-world clinical data. The goal is to catch as many positive cases as possible (prioritizing recall), as this would be critical in a medical screening context.

---

## 🧪 Dataset
- **Source**: Pima Indians Diabetes Dataset (UCI / Kaggle)
- 768 records, 8 features
- Target variable: `Outcome` (0 = no diabetes, 1 = diabetes)

---

## 🔧 Preprocessing
- Replaced medically invalid 0s with median values
- Scaled features using `StandardScaler`
- Applied **SMOTE** to balance class distribution

---

## 🧠 Models Tested
- Neural Network (Keras)
- Random Forest
- XGBoost
- Ensemble (average probabilities from all 3)

---

## ✅ Threshold Tuning
- Lowered sigmoid threshold to `0.3` to improve **recall**
- Focused on minimizing **false negatives**

---

## 🔍 Feature Importance
- Analyzed using:
  - Permutation Importance
  - SHAP (Deep + Model-Agnostic Explainer)

---

## 🏆 Final Ensemble Performance (threshold = 0.3)

| Metric       | Value |
|--------------|--------|
| Precision    | 0.71   |
| **Recall**   | **0.97** |
| F1 Score     | 0.82   |
| False Negatives | **3** out of 101 positives |

> Ensemble = Neural Net + Random Forest + XGBoost

---

## 📌 Key Takeaways
- Threshold tuning is essential in high-risk classification tasks
- Ensemble models can improve both stability and performance
- Feature analysis helps balance model complexity with impact

---

## 🚀 Future Ideas
- Try logistic regression + calibrated probabilities
- Deploy as an API with FastAPI or Flask
- Build a basic UI for risk flagging and interpretation

# diabetes-prediction-ensemble
