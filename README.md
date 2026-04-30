# ❤️ Heart Disease — EDA & Feature Engineering

## 📌 Objective

Heart disease is one of the leading causes of death globally. This project analyzes **which clinical features are most predictive of heart disease** and prepares a clean, ML-ready dataset using statistical feature selection.

---

## 📂 Dataset

| Detail | Info |
|--------|------|
| File | `heart.csv` |
| Rows | 918 |
| Features | Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope, HeartDisease |
| Target | `HeartDisease` (0 = No, 1 = Yes) |

---

## 🔍 What I Did

### 1. Data Cleaning
- Checked and handled null values
- Removed inconsistent entries (zero cholesterol etc.)
- Standardized data types across columns

### 2. Exploratory Data Analysis
- Age distribution across heart disease positive/negative groups
- Chest pain type analysis — ASY type most linked to heart disease
- ST Slope and Exercise Angina patterns explored visually

### 3. Feature Engineering
- One-hot encoded categorical columns: `Sex`, `ChestPainType`, `RestingECG`, `ST_Slope`, `ExerciseAngina`
- Created binary columns for cleaner ML compatibility
- Built encoded dataframe `df_encode` for statistical testing

### 4. Feature Selection (Chi-Square Test)

| Feature | Chi² Score | Decision |
|---------|-----------|----------|
| ST_Slope_Up | 352.82 | ✅ Keep |
| ST_Slope_Flat | 279.66 | ✅ Keep |
| ExerciseAngina_Y | 222.26 | ✅ Keep |
| ChestPainType_ATA | 146.24 | ✅ Keep |
| Sex_M | 84.15 | ✅ Keep |
| ChestPainType_NAP | 40.61 | ✅ Keep |
| RestingECG_ST | 9.14 | ✅ Keep |
| RestingECG_Normal | 7.33 | ✅ Keep |
| ChestPainType_TA | 2.27 | ❌ Drop |

### 5. Final Dataset
- Created `final_df` with only statistically significant features
- Ready for classification model training

---

## 📊 Key Findings

- 📉 **ST Slope** (Up/Flat) is the strongest predictor of heart disease
- 🏃 **Exercise-induced Angina** is highly significant
- 💢 **Chest Pain Type** — ASY type most associated with disease
- 👨 **Male sex** shows higher heart disease risk in this dataset
- 🫀 **RestingECG** has moderate but significant predictive power

---

## 🔜 Next Steps

- Build a **Logistic Regression** classifier
- Try **Random Forest** and compare accuracy
- Evaluate with Confusion Matrix, Precision, Recall, F1 Score

---

## 📁 Files

| File | Description |
|------|-------------|
| `Heart_Disease_EDA_Analysis.ipynb` | Main notebook with full analysis |
| `heart.csv` | Raw dataset |

---

## 👤 Author

**Vikas Singh** — Ops Specialist transitioning into AI/ML  
🔗 [LinkedIn](https://linkedin.com/in/build-with-vikas) · [GitHub](https://github.com/build-with-vikas)
