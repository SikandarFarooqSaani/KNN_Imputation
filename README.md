# KNN_Imputation
# 🤖 KNN Imputer — AI Generated Report

## 📘 Overview
This section explains the use of **KNN Imputer** for handling missing values in the **Titanic dataset**.  
The goal is to compare its performance against simple imputation techniques using a Logistic Regression model.

---

## ⚙️ Steps and Process

### **1. Dataset**
- Dataset: **Titanic** (available in the repository)
- Columns used:
  - `Age`
  - `Pclass`
  - `Fare`

---

### **2. Data Information**
- `Age` column has approximately **19% missing values**.
- Other selected columns are complete and suitable for training.

---

### **3. Data Preparation**
- Performed **Train-Test Split** to ensure proper model evaluation and avoid data leakage.

---

### **4. Applying KNN Imputer**
- Used **KNN Imputer** with:
  - `n_neighbors = 5`
  - `weights = 'distance'`
- The imputer replaces missing values based on the **weighted average** of the nearest neighbors (closer neighbors have more influence).

---

### **5. Conversion**
- The transformed NumPy array after imputation was **converted back to a DataFrame** to maintain readability and structure.

---

### **6. Model Training & Evaluation**
Two imputation strategies were compared using **Logistic Regression**:

| Imputation Method | Accuracy |
|--------------------|-----------|
| Simple Imputer | 0.69 |
| KNN Imputer | **0.70** |

✅ **KNN Imputer performed slightly better**, showing its advantage in preserving data relationships through neighbor-based estimation.

---

## 🔍 Key Insights
- **KNN Imputer** estimates missing values using similarity between rows (based on nearest neighbors).
- Since it considers feature correlation, it often gives **better accuracy** than simple mean/median imputation.
- However, it is **computationally more expensive** and may slow down with large datasets.
- Works best when features have **strong relationships**, as seen between `Age`, `Pclass`, and `Fare`.

---

## 🧩 Attachments
- **Dataset:** Titanic dataset (included in repository)  
- **Model:** Logistic Regression  
- **Imputer Used:** KNN Imputer (`n_neighbors=5`, `weights='distance'`)

---

> ⚠️ *This README is AI-generated to summarize the KNN Imputer implementation and its performance comparison on the Titanic dataset.*

