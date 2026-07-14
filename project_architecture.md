
# 🏗️ Project Architecture

                     ┌─────────────────────────┐
                     │  California Housing     │
                     │       Dataset           │
                     └──────────┬──────────────┘
                                │
                                ▼
                  ┌───────────────────────────┐
                  │ Load Dataset (Pandas)     │
                  └──────────┬────────────────┘
                             │
                             ▼
          ┌─────────────────────────────────────┐
          │ Create Income Categories            │
          │ (for Stratified Sampling)           │
          └──────────┬──────────────────────────┘
                     │
                     ▼
       ┌─────────────────────────────────────────┐
       │ Stratified Train-Test Split             │
       └──────────┬──────────────────────────────┘
                  │
                  ▼
     ┌───────────────────────────────────────────┐
     │ Separate Features (X) & Target (y)        │
     └──────────┬────────────────────────────────┘
                │
      ┌─────────┴─────────┐
      ▼                   ▼
┌───────────────┐   ┌────────────────────┐
│ Numerical     │   │ Categorical        │
│ Features      │   │ Features           │
└──────┬────────┘   └─────────┬──────────┘
       │                      │
       ▼                      ▼
┌───────────────────┐   ┌───────────────────┐
│ Median Imputation │   │ One-Hot Encoding  │
└─────────┬─────────┘   └─────────┬─────────┘
          │                       │
          ▼                       │
┌───────────────────┐             │
│ Standard Scaling  │             │
└─────────┬─────────┘             │
          └───────────┬───────────┘
                      ▼
        ┌─────────────────────────────┐
        │ ColumnTransformer           │
        │ (Combine Pipelines)         │
        └────────────┬────────────────┘
                     │
                     ▼
        ┌─────────────────────────────┐
        │ Machine Learning Ready Data │
        │ (NumPy Array)               │
        └────────────┬────────────────┘
                     │
                     ▼
      ┌─────────────────────────────────┐
      │ Regression Models               │
      │ • Linear Regression             │
      │ • Decision Tree                 │
      │ • Random Forest                 │
      └─────────────────────────────────┘
```

### Architecture Components

* **Dataset:** California Housing Dataset is loaded using Pandas.
* **Stratified Sampling:** Income categories are created to ensure balanced train-test splitting.
* **Feature Separation:** The target variable (`median_house_value`) is separated from the input features.
* **Numerical Pipeline:** Missing values are filled using median imputation, followed by feature scaling with `StandardScaler`.
* **Categorical Pipeline:** The `ocean_proximity` feature is converted into numerical format using `OneHotEncoder`.
* **ColumnTransformer:** Combines both preprocessing pipelines into a single workflow.
* **Output:** Produces a fully numeric, machine-learning-ready dataset that can be directly used for training regression models.

---


