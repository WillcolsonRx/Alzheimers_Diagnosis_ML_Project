# 🧠 Alzheimer’s Disease Diagnosis Using Explainable Machine Learning

This project applies multiple supervised machine learning techniques to a clinical dataset to **predict Alzheimer’s disease** and identify the **most influential clinical features** contributing to the diagnosis.  
Algorithms such as Random Forest, XGBoost, SVM, Logistic Regression, and a Neural Network were evaluated, followed by advanced explainability techniques including **Permutation Importance** and **SHAP**.

---

## 📌 Project Objectives
- Build machine learning models to classify patients as **Alzheimer’s or non-Alzheimer’s**.
- Compare and evaluate multiple algorithms using clinical data.
- Identify the **key clinical predictors** influencing Alzheimer’s diagnosis.
- Provide **interpretable explanations** using SHAP to ensure transparency and clinical relevance.

---

## 📘 Dataset Description
- **Total patients:** 2,149  
- **Total features:** 32 clinical features  
- **Target variable:** `Diagnosis` (0 = No AD, 1 = AD)  
- Features include:
  - Cognitive scores (MMSE, FunctionalAssessment)
  - Daily living functionality (ADL)
  - Memory and behavioral symptoms
  - Lifestyle and metabolic factors
  - Vitals and lab measurements
  - Demographics

---

## 🚀 Machine Learning Models Used
The following models were trained and evaluated:

- Logistic Regression  
- Gaussian Naive Bayes  
- Decision Tree  
- **Random Forest (Best Performing Model)**  
- XGBoost  
- Support Vector Machine (SVM)  
- Neural Network (MLP)

---

## 🏆 Model Performance Summary (Random Forest – Best Model)

| Metric        | Score  |
|---------------|--------|
| **Accuracy**  | 0.878  |
| **Precision** | 0.865  |
| **Recall**    | 0.893  |
| **F1-score**  | 0.879  |
| **ROC-AUC**   | **0.951** |

**Interpretation:**  
The Random Forest model shows excellent diagnostic performance with a very high ROC-AUC of **0.951** and a strong recall of **0.893**, meaning it reliably identifies Alzheimer’s patients while keeping false negatives low.

---

## 🔍 Key Feature Importance Results

### 🟩 **Top Predictors of Alzheimer’s Disease**
(Consistent across Random Forest, Permutation Importance & SHAP)

1. **FunctionalAssessment**
2. **ADL (Activities of Daily Living)**
3. **MMSE (Mini-Mental State Examination)**
4. **MemoryComplaints**

These features contribute the majority of diagnostic signal and are clinically well-established markers of Alzheimer’s disease.

### 🟨 Moderate Contributors
- BehavioralProblems  
- DietQuality  
- PhysicalActivity  
- SleepQuality  
- BMI  
- Cholesterol levels (HDL, LDL, Total, Triglycerides)

### 🟥 Low-Importance Features
- Gender  
- Ethnicity  
- Smoking  
- Depression  
- Hypertension  
- Diabetes  
- HeadInjury  

---

## 🧠 Explainability Methods

### ✔ **Permutation Importance**
Used to measure the actual impact of each feature on model performance.

### ✔ **SHAP (SHapley Additive exPlanations)**
Provides:
- Global importance (which features matter most)
- Local explanations (why an individual patient was predicted as AD or non-AD)
- Directional influence (whether high/low values increase AD risk)

SHAP visualizations clearly highlighted **FunctionalAssessment**, **ADL**, and **MMSE** as the strongest contributors.

---

## 📂 Project Structure
