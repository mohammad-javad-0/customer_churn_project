# ```markdown

# \# Telco Customer Churn Prediction

# 

# This repository contains an end-to-end Machine Learning project aimed at predicting customer churn for a telecommunications company. By analyzing customer behavior and demographics, the goal is to identify individuals at a high risk of churning, enabling proactive retention strategies.

# 

# The dataset used in this project was sourced from \*\*Kaggle\*\* (\[Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blaiseabatcha/telco-customer-churn-csv)).

# 

# \## Project Structure

# 

# ```text

# ├── data/

# │   └── Telco-Customer-Churn.csv   # Dataset from Kaggle

# ├── model/

# │   └── final\_model.pkl            # Trained and serialized final pipeline

# ├── eda.ipynb                      # Exploratory Data Analysis \& Visualization

# ├── training.ipynb                 # Preprocessing, Model Training \& Selection

# └── README.md                      # Project Documentation

# 

# ```

# 

# \## Data \& Feature Overview

# 

# The dataset contains \*\*7,032 entries\*\* with 20 features covering:

# 

# \* \*\*Demographics:\*\* Gender, Senior Citizen status, Partner, Dependents.

# \* \*\*Customer Account Info:\*\* Tenure (months with the company), Contract type, Paperless Billing, Payment Method, Monthly Charges, Total Charges.

# \* \*\*Services Signed Up For:\*\* Phone Service, Multiple Lines, Internet Service (DSL/Fiber optic), Online Security, Online Backup, Device Protection, Tech Support, Streaming TV, Streaming Movies.

# \* \*\*Target:\*\* `Churn` (Yes/No) indicating whether the customer left within the last month.

# 

# \## Exploratory Data Analysis (EDA) Highlights

# 

# Key insights discovered during EDA (`eda.ipynb`):

# 

# \* \*\*Class Imbalance:\*\* The target variable `Churn` is imbalanced, with roughly 73.4% "No" and 26.6% "Yes" observations.

# \* \*\*Tenure Influence:\*\* Customers with shorter tenures exhibit a significantly higher churn rate, heavily concentrated in the first few months of service.

# \* \*\*Charges vs. Churn:\*\* Higher monthly charges generally correlate with an increased likelihood of churn, especially among customers using Fiber Optic internet services.

# 

# \##text Preprocessing \& Feature Engineering

# Before training the predictive models, the following pipeline was built (`training.ipynb`):

# 

# 1\. \*\*Index Assignment:\*\* Set `customerID` as the DataFrame index since it represents unique records.

# 2\. \*\*Categorical Encoding:\*\* Applied `OneHotEncoder(handle\_unknown='ignore')` to convert all categorical attributes into numerical formats.

# 3\. \*\*Feature Scaling:\*\* Implemented `StandardScaler()` specifically for models requiring feature scaling (e.g., Logistic Regression, Support Vector Classifiers).

# 4\. \*\*Handling Imbalance:\*\* Integrated `class\_weight='balanced'` within the classification algorithms to counter the negative effects of class imbalance.

# 

# \## Model Evaluation \& Hyperparameter Tuning

# 

# We evaluated multiple foundational and ensemble classification algorithms using a 5-fold `StratifiedKFold` cross-validation scheme over a grid search parameter sweep (`GridSearchCV`):

# 

# \* Logistic Regression (with SAGA solver)

# \* Support Vector Classifier (SVC)

# \* Random Forest Classifier

# \* AdaBoost Classifier

# \* Gradient Boosting Classifier

# 

# \### Final Selected Model

# 

# The \*\*Logistic Regression\*\* pipeline configured with balanced class weights, scaled input distributions, and tuned regularization bounds was chosen as the production architecture. It effectively balances sensitivity (recall) for predicting actual churn instances while mitigating high false-alarm rates.

# 

# The optimized end-to-end configuration was packaged via `sklearn.compose.ColumnTransformer` and serialized using `joblib` into `model/final\_model.pkl` for immediate inference deployment.

# 

# \## Getting Started

# 

# \### Prerequisites

# 

# Make sure you have the following libraries installed:

# 

# ```bash

# pip install numpy pandas matplotlib seaborn scikit-learn joblib

# 

# ```

# 

# \### Running the Notebooks

# 

# 1\. Clone this repository:

# ```bash

# git clone \[https://github.com/mohammad-javad-0/customer\_churn\_project.git](https://github.com/mohammad-javad-0/customer\_churn\_project.git)

# cd customer\_churn\_project

# 

# ```

# 

# 

# 2\. Explore data insights by opening `eda.ipynb`.

# 3\. Re-train or inspect the ML workflows through `training.ipynb`.

# 

# \## License

# 

# This project is open-source and available under the MIT License.

# 

# ```

