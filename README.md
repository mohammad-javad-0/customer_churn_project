# Customer Churn Prediction Project

Predicting customer churn using Machine Learning techniques on the Telco Customer Churn dataset.

## Project Overview

Customer churn is one of the most important challenges for subscription-based businesses. In this project, we analyze customer behavior and build machine learning models to predict whether a customer is likely to leave the service.

The project includes:

* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Model Training & Evaluation
* Hyperparameter Tuning
* Final Model Selection

---

## Repository Structure

```text
customer_churn_project/
│
├── Telco-Customer-Churn.csv      # Dataset
├── eda.ipynb                     # Exploratory Data Analysis
├── training.ipynb                # Model Training & Evaluation
├── README.md
```

---

## Dataset

Dataset: Telco Customer Churn

The dataset contains customer demographic information, account details, subscribed services, and churn status.

### Target Variable

* **Churn**

  * Yes → Customer left the company
  * No → Customer stayed

### Example Features

* Gender
* SeniorCitizen
* Partner
* Dependents
* Tenure
* InternetService
* Contract
* PaymentMethod
* MonthlyCharges
* TotalCharges

---

## Exploratory Data Analysis

The EDA notebook includes:

* Missing value analysis
* Data type inspection
* Target distribution analysis
* Customer behavior exploration
* Numerical feature analysis
* Categorical feature analysis
* Correlation and business insights

---

## Data Preprocessing

The preprocessing pipeline includes:

* Handling missing values
* One-Hot Encoding for categorical features
* Feature scaling for numerical features
* Train/Test split
* Pipeline-based workflow using Scikit-Learn

---

## Models Evaluated

Several classification algorithms were trained and compared:

* Logistic Regression
* Support Vector Machine (SVC)
* Random Forest
* AdaBoost
* Gradient Boosting

Hyperparameter tuning was performed using **GridSearchCV** with cross-validation.

---

## Evaluation Metrics

Models were evaluated using:

* F1 Score
* Classification Report
* Confusion Matrix
* Cross-Validation Performance

The final selected model was chosen based on predictive performance and generalization ability.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* Jupyter Notebook

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/mohammad-javad-0/customer_churn_project.git
cd customer_churn_project
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install pandas numpy matplotlib scikit-learn
```

### 3. Run notebooks

```bash
jupyter notebook
```

Open:

* `eda.ipynb`
* `training.ipynb`

---

## Project Goal

The main objective of this project is to identify customers who are at risk of churn and provide a machine learning solution that can support customer retention strategies.
