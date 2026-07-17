Healthcare Insurance Cost Predictor

A machine learning regression project that predicts annual healthcare insurance charges based on demographic and lifestyle factors. The project follows a complete data science workflow — from exploratory data analysis to model comparison and hyperparameter tuning.


📌 Problem Statement

Healthcare insurance charges vary significantly across individuals due to factors such as age, BMI, smoking status, and region. Accurately predicting these costs helps insurance companies set fair premiums, manage financial risk, and improve pricing strategies.


🎯 Objectives


Perform exploratory data analysis (EDA) to understand the dataset
Preprocess and encode features using sklearn Pipelines
Train and compare multiple regression models
Tune hyperparameters using GridSearchCV
Select the best-performing model based on evaluation metrics



📁 Dataset

The dataset contains 1,338 records of insured individuals with the following features:

FeatureDescriptionAGEAge of the insured individualGenderGender of the insured individualBody_Mass_Index (BMI)Body Mass IndexNumber_of_ChildrenNumber of dependentsSmoking_StatusWhether the individual smokesRegionResidential regionInsurance_ChargesAnnual insurance cost — Target Variable


🛠️ Tech Stack


Python 3
pandas — data manipulation
NumPy — numerical operations
seaborn / matplotlib — data visualisation
scikit-learn — modelling, pipelines, and evaluation



⚙️ Project Workflow

Data Loading → EDA → Preprocessing → Model Training → Hyperparameter Tuning → Evaluation → Conclusion

Preprocessing


Missing values and duplicates checked and handled
Numerical features scaled using StandardScaler
Categorical features encoded using OneHotEncoder
All preprocessing wrapped in a ColumnTransformer inside sklearn Pipeline to prevent data leakage



🤖 Models Trained

ModelBaseline R²Tuned R²Ridge Regression0.7700.769Lasso Regression0.7650.770Decision Tree0.7740.872Random Forest0.8660.872

Hyperparameter tuning was performed using GridSearchCV with 5-fold cross-validation.


📊 Evaluation Metrics

Each model was evaluated using:


MAE — Mean Absolute Error
RMSE — Root Mean Squared Error
R² — Coefficient of Determination



✅ Best Model

Tuned Random Forest Regressor


RMSE: ~4,634
MAE: ~2,546
R²: 0.872


The Random Forest consistently outperformed all linear models by capturing non-linear relationships in the data — particularly the strong influence of smoking status on insurance charges.


🚀 How to Run


Clone the repository


bashgit clone https://github.com/brandonmutua/healthcare-insurance-cost-predictor.git
cd healthcare-insurance-cost-predictor


Install dependencies


bashpip install -r requirements.txt


Launch the notebook


bashjupyter notebook model.ipynb


📦 Requirements

pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter


Save these in a requirements.txt file in your repo root.




📂 Repository Structure

healthcare-insurance-cost-predictor/
│
├── model.ipynb          # Main Jupyter notebook
├── insurance.csv        # Dataset
├── requirements.txt     # Dependencies
└── README.md            # Project documentation


👤 Author

Your Name
GitHub · LinkedIn
