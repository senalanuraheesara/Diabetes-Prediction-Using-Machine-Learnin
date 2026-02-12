# 🩺 Diabetes Prediction Using Machine Learning

---

## 📌 Project Overview

Diabetes is a rapidly increasing global health issue. Early detection is essential to reduce complications and healthcare costs.

This project uses **Machine Learning classification models** to predict whether an individual is diabetic based on medical and demographic attributes.

---

## 🎯 Objective

To build and evaluate multiple ML models and select the most accurate and interpretable model for diabetes risk prediction.

---

## 📊 Dataset Information

- **Source:** NIDDK Healthcare Diabetes Dataset  
- **Records:** 2,768  
- **Features:** 9  
- **Target Variable:**
  - `0` → Non-Diabetic  
  - `1` → Diabetic  

### 🔎 Features Used

- Age  
- Gender  
- BMI  
- Blood Pressure  
- Glucose  
- Insulin  
- Physical Activity  
- Smoking History  
- Cholesterol  

---

## 🔍 Data Preprocessing

✔ No missing values  
✔ Outlier handling using Winsorization  
✔ One-Hot Encoding  
✔ Feature Scaling using StandardScaler  
✔ SMOTE applied for class imbalance  

---

## 🤖 Models Implemented

- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  
- Neural Network (MLP)  
- Logistic Regression  
- XGBoost  

---

## 📊 Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1 Score |
|--------|----------|-----------|--------|----------|
| 🏆 Decision Tree | **99%** | 100% | 98% | 99% |
| Random Forest | 98% | 99% | 97% | 98% |
| SVM | 97% | 99% | 93% | 96% |
| XGBoost | 93% | 93% | 93% | 93% |
| Logistic Regression | 78% | 68% | 73% | 71% |
| Neural Network (MLP) | 73% | 64% | 84% | 80% |

---

## 🏆 Final Selected Model: Decision Tree

The Decision Tree model was selected because:

- High Accuracy (99%)
- Excellent Recall (critical in healthcare)
- High Precision
- Transparent & Interpretable
- Suitable for clinical decision support systems

---

## ⚖️ Ethical Considerations

- Data anonymization maintained  
- Class imbalance handled using SMOTE  
- Recall prioritized to reduce false negatives  
- Designed with healthcare fairness in mind  

---

## 🧠 Key Insights

- BMI, Glucose, and Blood Pressure were the most influential predictors.  
- Recall is more important than accuracy in medical diagnosis.  
- Simpler models can outperform complex ones when tuned properly.  

---

## 🛠 Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib  
- Seaborn  
- Imbalanced-learn (SMOTE)  

---

## 🚀 Future Improvements

- External validation with larger datasets  
- SHAP/LIME for explainability  
- Deployment as a web-based healthcare tool  
- Integration with real-time clinical systems  

---

## 👨‍💻 Team Members

- Liyanage D C J  
- Disanayaka R M K S  
- Dissanayaka D. M. H  
- Punchihewa S.D  
- **Anuraheesara U.A.S**  
- Madhusanka S.P  

---

## 📚 References

- Kaggle Healthcare Diabetes Dataset  
- WHO Reports on Diabetes  
---

## 👨‍💻 Developed As

Artificial Intelligence & Machine Learning Project  
B.Sc. (Hons) in Information Technology – Year 2 Semester 1  
Sri Lanka Institute of Information Technology (SLIIT)

---
