# 🧠 Thyroid Disease Detection using Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/ML-Python-blue.svg"/>
  <img src="https://img.shields.io/badge/AWS-SageMaker-orange.svg"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen.svg"/>
</p>

## 🚀 Project Summary

This project presents a machine learning-based diagnostic tool for early detection of thyroid disease, developed using a healthcare dataset of over 9,000 patients. The pipeline is designed to be scalable, cloud-native, and reliable for binary classification (Thyroid Disease: Yes/No), leveraging AWS SageMaker and Random Forest for production-ready performance.

---

## 📊 Problem Statement

Thyroid disorders are common but underdiagnosed. This project aims to:
- Predict the presence of thyroid disease from hormone and demographic data
- Minimize false negatives to avoid missed diagnoses
- Build a pipeline suitable for healthcare deployment

---

## 🧰 Tech Stack

| Component      | Tools / Frameworks |
|----------------|--------------------|
| Language       | Python |
| ML Libraries   | Scikit-learn, PCA |
| Cloud Services | AWS SageMaker, Amazon S3 |
| Environment    | Jupyter Notebook |
| Algorithms     | Random Forest, Decision Tree, Logistic Regression |

---

## 📂 Dataset Overview

- **Records:** 9,000+ patients
- **Features:** TSH, T3, TT4, T4U, FTI, Age, Gender
- **Target:** Binary (Thyroid disease: Yes/No)
- **Challenges:** Missing values, class imbalance, noisy inputs

---

## 🧪 ML Workflow

1. **Data Preprocessing**
   - Median/Mode imputation
   - One-Hot Encoding
   - Stratified 80/20 train-test split

2. **Modeling**
   - 🔹 Logistic Regression (baseline)
   - 🔹 Decision Tree Classifier
   - 🔹 ✅ **Random Forest Classifier** (Best: AUC = 0.98)

3. **Dimensionality Reduction**
   - PCA to test performance vs. interpretability

4. **Model Evaluation**
   - ROC Curve, F1-Score, Confusion Matrix

---

## 📈 Results

| Model               | Accuracy | AUC   | Recall (Thyroid Cases) |
|--------------------|----------|-------|------------------------|
| Random Forest       | **94.2%** | **0.98** | **91.3%** ✅ |
| Decision Tree       | 92.0%    | 0.92  | 82.6% |
| Logistic Regression | 85.6%    | 0.81  | 53.3% ❌ |

📝 **Insight:** Random Forest delivered the best balance of sensitivity and accuracy — critical for real-world healthcare applications.

---

## 🌐 AWS SageMaker Integration

- 📤 Data uploaded to Amazon S3
- 📓 Notebook execution and model training in AWS SageMaker
- 📁 Models stored in `.joblib` format for reuse

---

## 🔍 Key Takeaways

✅ Built a production-scale ML pipeline on AWS  
✅ High-performing Random Forest model with 94.2% accuracy  
✅ Addressed model interpretability and PCA trade-offs  
✅ Ready for deployment via REST API or Streamlit

---

## 🧠 Future Enhancements

- 🔄 Automate pipeline using **AWS Step Functions**
- 🌲 Add **XGBoost and LightGBM** for comparison
- 🔍 Integrate **SHAP/LIME** for explainability
- ☁️ Deploy REST API or Streamlit app for real-time prediction

## 📎 Project Assets

- 📓 [Jupyter Notebook](./thyroid_prediction.ipynb)
- 📄 [Technical Report (PDF)](./Thyroid_Disease_Prediction_Report.pdf)
- 🖼️ [Presentation Slides (PDF)](./Thyroid_Disease_Prediction_Presentation.pdf)

