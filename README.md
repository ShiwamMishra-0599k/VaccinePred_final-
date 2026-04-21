# 💉 Vaccine Prediction — H1N1 & Seasonal Flu Classification

This project focuses on predicting whether individuals are likely to receive **H1N1 and Seasonal flu vaccines** using demographic, behavioral, and health-related data.

By applying machine learning models, this project identifies key factors influencing vaccination behavior and builds predictive systems that can support **public health decision-making and targeted vaccination campaigns**.

---

# ⚙️ Tech Stack

## Programming
- Python (Pandas, NumPy)
- Jupyter Notebook

## Data Visualization
- Matplotlib
- Seaborn

## Machine Learning
- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier
- Decision Tree
- Neural Network (MLP Classifier)

## Model Optimization
- GridSearchCV
- RandomizedSearchCV
- Cross-validation

---

# 📊 Data Source

Dataset provided by **DrivenData (Flu Shot Learning Dataset)**

## Dataset Overview

The dataset consists of survey responses capturing multiple aspects of individuals:

### 🔹 Feature Categories:
- **Demographics**: Age group, education, race, gender
- **Health Conditions**: Chronic illness, health insurance
- **Behavioral Patterns**: Preventive actions, hygiene habits
- **Opinions**: Vaccine effectiveness, perceived risk, side effects
- **Doctor Recommendation**: Whether a doctor recommended vaccination

### 🎯 Target Variables:
- `h1n1_vaccine` → Binary classification (0 = No, 1 = Yes)
- `seasonal_vaccine` → Binary classification (0 = No, 1 = Yes)

---

# 🎯 Problem Statement

## Objective
To build classification models that predict:

- Likelihood of **H1N1 vaccine uptake**
- Likelihood of **Seasonal flu vaccine uptake**

based on behavioral, demographic, and health-related attributes.

---

# 🧩 Task Breakdown

- Task 1: Perform Exploratory Data Analysis (EDA)
- Task 2: Handle missing values and preprocess dataset
- Task 3: Build multiple classification models
- Task 4: Evaluate models using appropriate metrics
- Task 5: Compare performance and select best model
- Task 6: Extract insights for public health strategies

---

# 🎯 Goal of the Project

- Identify key drivers behind vaccination decisions  
- Understand behavioral patterns influencing vaccine uptake  
- Build predictive models for healthcare applications  
- Compare performance of classification algorithms  
- Provide actionable insights for vaccination campaigns  

---

# 🚀 Solution Approach

## ✔ Step 1: Data Cleaning
- Removed duplicate records  
- Handled missing values:
  - Categorical features → Mode imputation  
  - Numerical features → Median imputation  
- Treated high-missing survey columns carefully  
- Ensured data consistency across features  

---

## ✔ Step 2: EDA & KPI Analysis
- Missing value heatmaps  
- Distribution analysis of opinion features  
- Demographic vs vaccination trends  
- Correlation analysis  
- Class imbalance analysis  

### 🔍 Key Observations:
- H1N1 dataset is **highly imbalanced (~21% vaccinated)**  
- Seasonal vaccine is relatively balanced (~46%)  
- Doctor recommendation strongly influences vaccination  
- Risk perception increases likelihood of vaccination  

---

## ✔ Step 3: Feature Engineering
- Categorized features into:
  - Numerical  
  - Categorical  
  - Binary  

- Applied:
  - One-hot encoding for categorical variables  
  - Feature scaling for neural networks  

- Built preprocessing pipelines using:
  - `ColumnTransformer`
  - `Pipeline`

---

## ✔ Step 4: Model Development

Trained multiple models:
- Logistic Regression  
- Random Forest  
- XGBoost  
- Decision Tree  
- Neural Network (MLP Classifier)  

Applied:
- Hyperparameter tuning  
- Stratified train-test split  
- Cross-validation  

---

## ✔ Step 5: Evaluation

Models evaluated using:
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC-AUC (primary metric due to class imbalance)  

---

# 📈 Model Performance

## 🔹 H1N1 Vaccine Prediction

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|------|---------|----------|--------|----------|--------|
| XGBoost | 0.84 | 0.68 | 0.46 | 0.55 | **0.83** |
| Logistic Regression | 0.83 | 0.66 | 0.47 | 0.55 | 0.83 |
| MLP | 0.83 | 0.67 | 0.43 | 0.53 | 0.82 |
| Random Forest | 0.83 | 0.74 | 0.31 | 0.45 | 0.82 |
| Decision Tree | 0.82 | 0.64 | 0.43 | 0.51 | 0.80 |

✅ **Best Model: XGBoost**
- Highest ROC-AUC
- Better balance between precision and recall

---

## 🔹 Seasonal Vaccine Prediction

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|------|---------|----------|--------|----------|--------|
| XGBoost | 0.78 | 0.78 | 0.74 | 0.76 | **0.86** |
| Logistic Regression | 0.78 | 0.74 | 0.74 | 0.76 | 0.85 |
| MLP | 0.78 | 0.73 | 0.73 | 0.75 | 0.85 |
| Random Forest | 0.78 | 0.73 | 0.73 | 0.76 | 0.83 |
| Decision Tree | 0.75 | 0.79 | 0.63 | 0.70 | 0.82 |

✅ **Best Model: XGBoost**
- Strong predictive performance
- Handles non-linear relationships effectively

---

# 🔍 Key Insights & Findings

- 🧑‍⚕️ Doctor recommendation is the **strongest predictor**
- ⚠️ Higher perceived risk → higher vaccination likelihood  
- 📊 Class imbalance significantly affects recall (H1N1)  
- 🌳 Tree-based models outperform linear models  
- 🧠 Behavioral and opinion-based features are highly influential  

---

# ⚠️ Challenges & Solutions

| Challenge | Solution |
|----------|---------|
| High missing values (survey data) | Mode/median imputation |
| Class imbalance (H1N1 dataset) | Used ROC-AUC and F1-score |
| Mixed data types | ColumnTransformer pipelines |
| Overfitting | Cross-validation and tuning |
| Feature complexity | Structured preprocessing pipelines |

---

# 💡 Impact & Applications

- 🏥 Public health policy planning  
- 🎯 Targeted vaccination campaigns  
- 📊 Population risk segmentation  
- 🤖 AI-driven healthcare recommendations  
- 📉 Reducing vaccine hesitancy  

---


---

# 🏁 Conclusion

This project demonstrates the application of machine learning in healthcare analytics to predict vaccination behavior.

Using advanced models like XGBoost along with strong preprocessing pipelines, the project delivers reliable predictions and actionable insights that can support real-world public health initiatives.
