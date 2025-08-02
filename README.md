# HR-Employee-Attrition-Prediction
HR Employee Attrition Prediction
This project focuses on analyzing and predicting employee attrition within a company using machine learning techniques. Employee attrition, or turnover, is a critical concern for businesses as it can lead to significant costs related to recruitment, training, and lost productivity. By understanding the factors that contribute to attrition and building predictive models, companies can proactively address issues and retain valuable talent.

The analysis is performed using a dataset containing various employee attributes. Different machine learning models are explored, evaluated, and the best-performing model is saved for future use.

## Table of Contents
 * HR Employee Attrition Prediction

 * Table of Contents

 * Project Overview

 * Dataset

 * Features

 * Analysis and Methodology

    * Data Loading and Initial Inspection

    * Data Preprocessing

    * Exploratory Data Analysis (EDA)

    * Model Training and Evaluation

    * Model Saving

* Results

* Installation

* Usage

* Contributing

* License

* Contact

## Project Overview
The main goals of this project are:

1. To perform exploratory data analysis (EDA) to understand the underlying patterns and relationships within the employee attrition dataset.

2. To preprocess the data, including handling categorical variables and scaling numerical features.

3. To build and train various classification models to predict employee attrition.

4. To evaluate the performance of these models using appropriate metrics.

5. To save the best-performing model for deployment or further analysis.

## Dataset
The dataset used for this project is WA_Fn-UseC_-HR-Employee-Attrition.csv. It contains information about employees and whether they have attrited (left the company) or not.

## Features
The dataset includes 35 columns, representing various employee attributes such as:

Age

Attrition (Target variable: Yes/No)

BusinessTravel

DailyRate

Department

DistanceFromHome

Education

EducationField

EnvironmentSatisfaction

Gender

HourlyRate

JobInvolvement

JobLevel

JobRole

JobSatisfaction

MaritalStatus

MonthlyIncome

MonthlyRate

NumCompaniesWorked

Over18

OverTime

PercentSalaryHike

PerformanceRating

RelationshipSatisfaction

StandardHours

StockOptionLevel

TotalWorkingYears

TrainingTimesLastYear

WorkLifeBalance

YearsAtCompany

YearsInCurrentRole

YearsSinceLastPromotion

YearsWithCurrManager

The columns EmployeeCount and EmployeeNumber were dropped as they were identified as having no predictive power or being constant.

## Analysis and Methodology
The project follows a standard machine learning pipeline:

## Data Loading and Initial Inspection
The dataset is loaded using pandas. Initial checks include viewing the first few rows (df.head()), checking the dimensions (df.shape), and inspecting for missing values (df.isnull().sum()). The dataset contains 1470 rows and 35 columns, with no missing values.

## Data Preprocessing
Feature Engineering: The notebook removes EmployeeCount and EmployeeNumber columns.

Categorical Encoding: Categorical features are converted into numerical representations using techniques like Label Encoding or One-Hot Encoding (though the provided snippet mainly shows initial data loading and basic checks, this would typically be a subsequent step).

Feature Scaling: Numerical features are scaled to ensure that no single feature dominates the model training due to its magnitude.

## Exploratory Data Analysis (EDA)
EDA is performed to gain insights into the data. Key visualizations include:

Attrition Distribution: Checking the balance of the target variable (df.Attrition.value_counts()). The dataset shows an imbalance, with 'No' attrition being significantly higher than 'Yes'.

Age Distribution of Attrited Employees: A histogram (sns.histplot) is used to visualize the age distribution of employees who left the company.

Department-wise Attrition: A histogram is used to show the number of people who left from each department.

Job Satisfaction vs. Attrition: A histogram is used to analyze the distribution of job satisfaction among employees who left.

## Model Training and Evaluation
The notebook mentions the use of various machine learning models (e.g., Logistic Regression, Decision Tree, Random Forest, XGBoost) and hyperparameter tuning using GridSearchCV. The models are evaluated using metrics such as accuracy, precision, recall, and F1-score, with a focus on the F1-score for the 'Yes' class due to class imbalance.

## Model Saving
The best-performing model (e.g., XGBoost) is saved using joblib for future use.

## Results
The analysis provides insights into the factors influencing employee attrition. The trained models offer predictive capabilities, with the XGBoost model showing promising performance (e.g., F1-score of 0.43 for the 'Yes' class).

## Installation
To run this project locally, you'll need Python and the following libraries:

pip install pandas numpy scikit-learn matplotlib seaborn joblib xgboost

## Usage
Clone the repository:

git clone https://github.com/your-username/HR-Employee-Attrition-Prediction.git
cd HR-Employee-Attrition-Prediction

Place the WA_Fn-UseC_-HR-Employee-Attrition.csv dataset in the project root directory.

Open the Jupyter Notebook:

jupyter notebook WA_Fn_UseC__HR_Employee_Attrition.ipynb

Run all cells in the notebook to execute the analysis, train models, and save the best model.

## Contributing
Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please open an issue or submit a pull request.

