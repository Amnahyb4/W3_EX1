
# 🧠 Predictive Modeling with scikit-learn (MOOC Exercises)

This repository contains my solutions and experiments for the **scikit-learn MOOC** on predictive modeling.  
It covers the full machine learning pipeline, from **data exploration** to **model evaluation and hyperparameter tuning**, using real-world datasets.

---

##  Covered Modules & Exercises

### 🔹 Module M1 — Predictive Modeling Pipeline

#### **M1.01 – Tabular Data Exploration**
- Loaded and explored tabular datasets using **pandas**
- Identified **features vs target**
- Distinguished **numerical vs categorical** variables
- Explored class distributions
- Visualized feature distributions using:
  - Histograms
  - Pair plots (seaborn)

📂 Dataset:
- `penguins_classification.csv`

---

#### **M1.02 – First Model on Numerical Data**
- Built a first classifier using **KNeighborsClassifier**
- Learned how to use:
  - `fit()`
  - `predict()`
  - `score()`
- Investigated default hyperparameters (`n_neighbors`)
- Performed a **train-test split**

📂 Dataset:
- `adult-census-numeric.csv`

---

#### **M1.03 – Baseline Models & Model Evaluation**
- Introduced **baseline models** using `DummyClassifier`
- Compared model performance against:
  - Always predicting the majority class
- Discussed whether ~81–82% accuracy is meaningful
- Evaluated generalization using **train/test split**

📂 Dataset:
- `adult-census.csv`

---

#### **M1.04 – Handling Categorical Data**
- Worked with **categorical variables**
- Used:
  - `OrdinalEncoder`
  - `OneHotEncoder`
- Built **pipelines** with `LogisticRegression`
- Evaluated models using **cross-validation**
- Observed that:
  - One-hot encoding performs better for linear models
  - Ordinal encoding can introduce artificial ordering

> **Key insight:**  
> Categorical features do **not** have an inherent order → `OneHotEncoder` is usually more appropriate for linear models.

---

#### **M1.05 – Numerical + Categorical Features Together**
- Used **ColumnTransformer** to:
  - Scale numerical features
  - Encode categorical features
- Compared preprocessing strategies for:
  - Linear models
  - Tree-based models
- Learned that:
  - Tree-based models do **not** require feature scaling
  - Ordinal encoding is acceptable for trees

Models used:
- `LogisticRegression`
- `HistGradientBoostingClassifier`

---

### 🔹 Module M2 — Model Validation

#### **Cross-Validation**
- Used `cross_validate`
- Understood the difference between:
  - Training score
  - Test score
- Learned that cross-validation is used for:
  - Estimating **generalization performance**
  - Measuring **performance uncertainty**
- Analyzed:
  - Mean accuracy
  - Standard deviation
  - Fit time vs score time

📂 Dataset:
- `blood_transfusion.csv`

---

### 🔹 Module M3 — Hyperparameter Tuning

#### **M3.01 – Manual Hyperparameter Tuning**
- Performed **manual search** over hyperparameters
- Tuned parameters for:
  - Tree-based models
- Used:
  - Smaller training subsets for faster iteration
  - `train_size` to control computation cost

Model:
- `HistGradientBoostingClassifier`

---

## Technologies Used

- Python 3.11
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- Jupyter Notebooks

---

## 📁 Repository Structure

```text
.
├── dataset/
│   ├── adult-census.csv
│   ├── adult-census-numeric.csv
│   ├── blood_transfusion.csv
│   └── penguins_classification.csv
│
├── 01_tabular_data_exploration_ex_01.ipynb
├── 02_numerical_pipeline_ex_01.ipynb
├── 03_categorical_pipeline_ex_01.ipynb
├── 03_categorical_pipeline_ex_02.ipynb
├── cross_validation_ex_01.ipynb
├── parameter_tuning_ex_01.ipynb
├── parameter_tuning_ex_02.ipynb
└── README.md

##  Learning Outcomes

- Built end-to-end machine learning pipelines using scikit-learn  
- Explored and prepared tabular data with numerical and categorical features  
- Applied appropriate encoding strategies and preprocessing techniques  
- Evaluated models using cross-validation and baseline comparisons  
- Performed hyperparameter tuning and analyzed model performance  
