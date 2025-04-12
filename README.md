# Feature Engineering & Preprocessing

This project involves end-to-end feature engineering and preprocessing on a customer churn dataset containing **9134 rows** and **24 columns**. The goal is to prepare the data for machine learning tasks such as classification.

---

## 📁 Dataset Overview

- **Total Rows**: 9134  
- **Original Features**: 24  
- **Target Variable**: `Response`  
- **Date Column**: `EffectiveToDate`

---

## 🧰 Key Preprocessing Techniques Applied

### ✅ 1. Handling Categorical Features

- **Label Encoding**: For binary features like `Gender`, `VehicleSize`.
- **Ordinal Encoding**: For ordered features like `Coverage`, `Education`, `VehicleClass`.
- **One-Hot Encoding**: For nominal features like `Policy`, `SalesChannel`, and later `LocationCode`, `MaritalStatus`.



---

### ✅ 2. Date Feature Extraction

From the `EffectiveToDate` column, we extracted:
- `EffectiveMonth`
- `EffectiveDay`

These were added as separate features to capture seasonal behavior.

---

### ✅ 3. Feature Scaling

Applied multiple scalers for experimentation:
- `MinMaxScaler`
- `StandardScaler`
- `RobustScaler`

---

## 🔬 Feature Selection

Used **Chi-Square Test** to select relevant features.  
To ensure compatibility with the test:

---

## 📌 Final Output

- A fully preprocessed and feature-engineered dataset ready for modeling.
- Separation of feature selection logic (Chi-Square) and transformation logic (encoding & scaling).

---

## 📚 Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- seaborn, matplotlib (for EDA and visualization)

Install using:

```bash
pip install -r requirements.txt
