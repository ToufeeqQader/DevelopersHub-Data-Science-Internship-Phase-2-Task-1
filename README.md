# DevelopersHub-Data-Science-Internship-Phase-2-Task-1

# Task 1: Term Deposit Subscription Prediction (Bank Marketing)

## 📌 Objective
Predict whether a bank customer will subscribe to a term deposit as a result of a marketing campaign using classification models and explainable AI techniques.

---

## 📂 Dataset
- **Name:** Bank Marketing Dataset
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
- **File Used:** `bank-additional-full.csv`
- **Size:** 41,188 rows × 21 columns
- **Target Variable:** `y` — whether the client subscribed to a term deposit (`yes` / `no`)

---

## 🔧 Tools & Libraries
| Library | Purpose |
|---|---|
| `pandas`, `numpy` | Data loading and manipulation |
| `matplotlib`, `seaborn` | Data visualization |
| `scikit-learn` | Model training and evaluation |
| `shap` | Explainable AI (model interpretability) |

---

## 🚀 My Approach

### 1. Data Loading & Exploration
- Loaded the semicolon-separated CSV file
- Inspected shape, data types, and missing values
- Visualized target variable distribution (class imbalance observed)

### 2. Data Preprocessing
- Replaced `unknown` values with column mode
- Label encoded all categorical features
- Mapped target variable: `yes → 1`, `no → 0`

### 3. Exploratory Data Analysis (EDA)
- Plotted target class distribution
- Generated a correlation heatmap across all features

### 4. Model Building
Trained two classification models with 80/20 train-test split:
- **Logistic Regression** — baseline linear model
- **Random Forest Classifier** — ensemble tree-based model

### 5. Model Evaluation
Each model was evaluated using:
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)
- ROC Curve with AUC Score

### 6. Explainable AI (SHAP)
- Used `TreeExplainer` on the Random Forest model
- Generated SHAP Summary Bar Plot and Beeswarm Plot for global feature importance
- Generated SHAP Waterfall Plots for 5 individual predictions

---

## 📊 Results & Findings

| Model | F1 Score | AUC |
|---|---|---|
| Logistic Regression | ~0.45 | ~0.79 |
| Random Forest | ~0.52 | ~0.93 |

**Key Insights:**
- **Random Forest significantly outperformed Logistic Regression** with a much higher AUC (0.93 vs 0.79)
- **`duration`** (last contact duration) was the most important feature — longer calls strongly correlate with subscription
- **`euribor3m`** (Euro interbank rate) and **`nr.employed`** (number of employees) were also highly influential — indicating macroeconomic conditions affect customer decisions
- **`age`** and **`campaign`** (number of contacts) had moderate impact
- SHAP waterfall plots revealed that customers contacted fewer times and during favorable economic periods were more likely to subscribe

---

# Task 1: Term Deposit Subscription Prediction (Bank Marketing)

## 📌 Objective
Predict whether a bank customer will subscribe to a term deposit as a result of a marketing campaign using classification models and explainable AI techniques.

---

## 📂 Dataset
- **Name:** Bank Marketing Dataset
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
- **File Used:** `bank-additional-full.csv`
- **Size:** 41,188 rows × 21 columns
- **Target Variable:** `y` — whether the client subscribed to a term deposit (`yes` / `no`)

---

## 🔧 Tools & Libraries
| Library | Purpose |
|---|---|
| `pandas`, `numpy` | Data loading and manipulation |
| `matplotlib`, `seaborn` | Data visualization |
| `scikit-learn` | Model training and evaluation |
| `shap` | Explainable AI (model interpretability) |

---

## 🚀 My Approach

### 1. Data Loading & Exploration
- Loaded the semicolon-separated CSV file
- Inspected shape, data types, and missing values
- Visualized target variable distribution (class imbalance observed)

### 2. Data Preprocessing
- Replaced `unknown` values with column mode
- Label encoded all categorical features
- Mapped target variable: `yes → 1`, `no → 0`

### 3. Exploratory Data Analysis (EDA)
- Plotted target class distribution
- Generated a correlation heatmap across all features

### 4. Model Building
Trained two classification models with 80/20 train-test split:
- **Logistic Regression** — baseline linear model
- **Random Forest Classifier** — ensemble tree-based model

### 5. Model Evaluation
Each model was evaluated using:
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)
- ROC Curve with AUC Score

### 6. Explainable AI (SHAP)
- Used `TreeExplainer` on the Random Forest model
- Generated SHAP Summary Bar Plot and Beeswarm Plot for global feature importance
- Generated SHAP Waterfall Plots for 5 individual predictions

---

## 📊 Results & Findings

| Model | F1 Score | AUC |
|---|---|---|
| Logistic Regression | ~0.45 | ~0.79 |
| Random Forest | ~0.52 | ~0.93 |

**Key Insights:**
- **Random Forest significantly outperformed Logistic Regression** with a much higher AUC (0.93 vs 0.79)
- **`duration`** (last contact duration) was the most important feature — longer calls strongly correlate with subscription
- **`euribor3m`** (Euro interbank rate) and **`nr.employed`** (number of employees) were also highly influential — indicating macroeconomic conditions affect customer decisions
- **`age`** and **`campaign`** (number of contacts) had moderate impact
- SHAP waterfall plots revealed that customers contacted fewer times and during favorable economic periods were more likely to subscribe

---
## 👤 Author
**Toufeeq Qader**
Data Science Intern — DevelopersHub Corporation
