# 🏠 House price prediction model

**House price prediction model** is an end-to-end **data preprocessing pipeline** for housing price prediction.
The project focuses on preparing raw housing data into a **clean, structured, and machine-learning-ready format** using **Scikit-Learn pipelines**.

> *Because every smart home starts with clean data.*

---

## 🎯Objective
* Prepare raw housing data for machine learning.
* Perform stratified train–test splitting for balanced data distribution.
* Handle missing values using median imputation.
* Standardize numerical features using StandardScaler.
* Encode categorical features using OneHotEncoder.
* Build reusable preprocessing pipelines with Pipeline and ColumnTransformer.
* Generate a clean, consistent, and machine-learning-ready dataset.
* Follow industry-standard data preprocessing practices.

---

## 📌 Project Overview

Real-world datasets are messy. Before building any machine learning model, data must be:

* Split correctly
* Cleaned properly
* Transformed consistently

**Data Before Doors** demonstrates industry-standard practices for:

* Stratified train–test splitting
* Handling missing values
* Feature scaling
* Encoding categorical variables
* Building reusable preprocessing pipelines

This project uses the **California Housing Dataset**.

---

## 🧠 Key Concepts Used

* Stratified Sampling
* Feature Engineering
* Data Imputation
* Standardization
* One-Hot Encoding
* Pipelines & ColumnTransformer
* Train–Test Data Isolation

---

## 🗂️ Project Workflow

1. Load the housing dataset
2. Create income categories for stratified sampling
3. Split data into train and test sets
4. Separate features and target variable
5. Build numerical and categorical pipelines
6. Combine pipelines using `ColumnTransformer`
7. Transform raw data into model-ready format

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-Learn**

---

## 📁 Dataset

* **Name:** California Housing Dataset
* **Target Variable:** `median_house_value`
* **Categorical Feature:** `ocean_proximity`
* **Numerical Features:** All remaining attributes

---
## ⚙️ Preprocessing Steps

### 🔢 Numerical Features

* Missing values handled using **median imputation**
* Features scaled using **StandardScaler**

### 🔤 Categorical Features

* Encoded using **OneHotEncoder**
* Converts text categories into binary features

---

## 📦 Output

* Final processed data is a **NumPy array**
* Fully numeric and ready for:

  * Linear Regression
  * Decision Tree
  * Random Forest
  * Any Scikit-Learn model

---

## 🚀 How to Run

```bash
pip install pandas numpy scikit-learn
```

```bash
python Deployable.py
```

> Make sure `housing.csv` is in the same directory.

---

## 📈 Future Improvements

* Add regression models (Linear / Random Forest)
* Model evaluation using RMSE
* Cross-validation
* Model saving with `joblib`
* Deploy using Streamlit

---
## ✅Conclusion

* Successfully transformed raw housing data into a clean and structured format.
* Applied preprocessing techniques while preventing data leakage.
* Processed both numerical and categorical features using Scikit-Learn pipelines.
* Produced a fully numeric dataset ready for machine learning models.
* Improved the consistency, scalability, and reusability of the preprocessing workflow.
* Established a strong foundation for future model training, evaluation, and deployment.


## 👤 Author

**Ankit Pardeshi**
B.E. – Artificial Intelligence & Data Science

---

## ⭐ Final Note

This project emphasizes a critical ML principle:

> **Never open the doors to prediction before cleaning the data.**

Happy Learning 🚀
