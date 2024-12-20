 # MeXE402_Midterm_Atienza-Manalo
#### 
Both Linear Regression and Logistic Regression are foundational techniques in machine learning used for different types of problems. While they share similarities in their structure, they are applied to distinct tasks and have different mathematical foundations. This repository will serve as our midterm exam that is designed to assess our understanding of [Linear Regression](#linear-regression-salary-data-analysis) and [Logistic Regression](#logistic-regression-bank-marketing-campaign-analysis) through practical application on real-world datasets.

# Linear Regression: Salary Data Analysis

## Introduction
- Linear regression analysis is used to predict the value of a variable based on the value of another variable. The variable you want to predict is called the dependent variable. The variable you are using to predict the other variable's value is called the independent variable.

## Dataset Description
- This dataset contains information about salaries, years of experience, and other relevant factors. It's a suitable dataset for predicting salaries based on experience using linear regression.
  
- **Key Features**:
  - `Salary`:The corresponding salary of the employee (in dollars).
  - `Years of Experience`: The number of years an employee has worked in their field.
  - `Gender:`The gender of the employee (e.g., Male, Female, Non-binary).
  - `Education Level:` The highest level of education attained by the employee (e.g., High School, Bachelor’s Degree, Master’s Degree, Ph.D.).
  - `Job title`: The employee's position or title within their organization (e.g., Software Engineer, Data Analyst, Project Manager).
  -  `Age:` The age of the employee (in years).

-  **Dependent Variable**:
   - `Salary`:The corresponding salary of the employee (in dollars).
     
## Objective
- The objective of the Salary Dataset is to analyze the relationship between salaries and years of experience and to build predictive models using linear regression. The primary goal is to predict an individual's salary based on their years of experience and other relevant factors. This can help in understanding salary trends, making informed salary forecasts, and identifying patterns between experience and earnings.

# **Linear Regression Analysis**

### Data Preprocessing
- This guide outlines the preprocessing steps used to prepare data for analysis and predictions, especially for salary-based job categorization and predictions.

### 1. Categorize Job Titles by Salary
- Organize job titles in order of salaries from highest to lowest, simplifying data for analysis and helping to identify discrepancies and patterns across roles within the organization.
<p align="center">
<img alt = "Python" height="400" src="https://github.com/user-attachments/assets/01b6e44b-0bb3-4818-9d14-311457efb18d">

### 2. Remove Irrelevant Variables
- To improve prediction accuracy, remove irrelevant data such as age and gender. This helps reduce potential bias and focuses the dataset on relevant information for analysis.
<p align="center">
 <img alt = "Python" height="400" src="https://github.com/user-attachments/assets/cef660e9-a479-4495-8cf9-2d2a1969f6f8">

### 3. Convert Non-Numerical to Numerical Values
- Using Excel's 'Find and Replace' feature to convert job titles and educational levels into numerical values enhances data consistency. This allows for more accurate pay distribution analysis, helping linear regression predictions become more precise.
<h2 align="center">
<img alt = "Python" height="400" src="https://github.com/user-attachments/assets/55ddd932-ebe5-4241-bda6-039b81c31892">
 
 #### The following numerical values have been assigned to the Job Title:                      
 - **Intern** = 1
 - **Entry Level** = 2
 - **Junior** = 3
 - **Associate** = 4
 - **Mid-Level** = 5
 - **Senior** = 6
 - **Lead** = 7
 - **Manager** = 8
 - **Director** = 9
 - **Executive** = 10
   
####  The  Education Level is represented by :
- **Highschool** = 1
- **Bachelor’s** = 2
- **Master’s** = 3
- **PhD** = 4

### 4. Check for Missing Values
- During data preprocessing, examine rows and columns for missing values. Identify gaps to decide on handling methods, such as imputation, dropping, or interpolation, to improve data integrity.
<h2 align="center">
<img alt = "Python" width="600" src="https://github.com/user-attachments/assets/eaec1bb6-5731-4ec1-b96d-a4d1a1c2a618">

### 5. Handle Missing Values
- Clean data by correcting inaccuracies and inconsistencies, handling missing values, removing duplicates, and standardizing formats. Automating these tasks enhances data quality, leading to more reliable insights.
  ![image](https://github.com/user-attachments/assets/0bc2128b-c385-4d77-b15e-6ff014ba7eaa)


### Model Implementation
- This project utilizes libraries to perform data manipulation, preprocessing, and modeling to create a reliable machine learning model. The focus is on **linear regression** with model accuracy measured through R-squared and Adjusted R-squared values.

#### Libraries Used

- **Pandas**: For data manipulation and analysis, primarily reading, inspecting, and cleaning the dataset.
  - `pd.read_csv()`: Loads the dataset.
 ![image](https://github.com/user-attachments/assets/608c3062-c835-45ea-9ba6-e90ac5b15d74)
    
  - `dataset.isnull()`: Checks for missing values.
    
    ![image](https://github.com/user-attachments/assets/ae287bad-7f5b-4bf1-85e3-a5596b4c4d97)

  - `fillna()`: Fills missing values in the dataset.
    ![image](https://github.com/user-attachments/assets/d981de68-b57b-433f-817f-d36ecd0d5f0b)


- **Scikit-Learn**: For machine learning model creation and evaluation.
  
  - `train_test_split`: Splits the dataset into training and testing sets.
    ![image](https://github.com/user-attachments/assets/944c97ea-bba7-4df9-9377-7fe98cedd52d)

    Output: The function returns four sets: 

<h4 align="center">X_train: Contains the features of the training set.</small> </h2>
<h2 align="center">

![image](https://github.com/user-attachments/assets/7bebabbb-87f4-48e3-a614-53e0a5f4a9e3)


<h4 align="center">	X_test: Contains the features of the testing set.</small> </h2>
<h2 align="center">

![image](https://github.com/user-attachments/assets/2244072a-f900-4b2e-ab1d-dfd4d8baf578)


<h4 align="center">	y_train: Contains the target variable of the training set.</small> </h2>
<h2 align="center">

![image](https://github.com/user-attachments/assets/fc73a1a5-a60b-4e6d-a13f-c344a3fb0e19)


<h4 align="center">y_test: Contains the target variable of the testing set.</small></h2>

<h4 align="center">

![image](https://github.com/user-attachments/assets/04200141-d4e5-4e4d-ae1d-94b97754f686)

</h2>

- **LinearRegression**:Applies the linear regression model.
  
   <h4 align="center">
    
  ![image](https://github.com/user-attachments/assets/dab7521e-709d-4515-a6e9-981329eaa4d9)

  </h2>

- **R-squared and Adjusted R-squared**: Measures model accuracy.
  
<h4 align="center">
 
![image](https://github.com/user-attachments/assets/d712c426-d1da-4fa9-b525-90b04d048386)

  </h2>

- **Matplotlib** (`import matplotlib.pyplot as plt`):For data visualization.
   
 <h2 align="center">
  
 ![image](https://github.com/user-attachments/assets/09f9b569-1ec7-4f0e-9bc3-97b5608ccaa4)

 

  
### Making Predictions
- This line of code uses the trained model (`model`) to make a prediction on a new data point.  In this case, the values are: `education level = 2`, `job title = 7`, and `years of experience = 5`.  The `predict` method returns a predicted value, which in this case is `92877.53123063`. This predicted value represents the estimated salary for the given data point based on the model's learned relationship between the input features and the target variable.

   <h2 align="center">
    
  ![image](https://github.com/user-attachments/assets/05a5366e-6de5-461e-b25f-72d7fd23d477)


## Discussion
1. **R-squared (R²)**: 0.9226
   - R² explains how well the independent variables account for the variance in the dependent variable (salary).
   - 92.26% of the variability in salary is explained by the model. This is a high value, indicating that the model captures most of the determinants of salary.

2. **Adjusted R-squared**: 0.9223
   - Adjusted R² adjusts for the number of predictors in the model, penalizing the inclusion of irrelevant predictors that don’t improve predictive power.
   - 92.23% means that even after accounting for the complexity of the model, it still explains the majority of the variance in salary. The slight decrease from R² suggests that the number of predictors is appropriate and that the model isn’t overfitting.

### Interpretation

- The high R² and Adjusted R² values around 92% imply that model has strong predictive power. It captures almost all the variability in salary, leaving only about 8% unexplained, which could be due to factors not included in the model, such as industry type, company size, performance incentives, or location.In regression models, the coefficients represent the effect of each independent variable on the dependent variable. Each coefficient tells how much the dependent variable is expected to change when that particular independent variable increases by one unit while holding all other variables constant.

![image](https://github.com/user-attachments/assets/cb8fda32-e35e-47cd-a2d8-98dfc5d2c173)


---------------------
# Logistic Regression: Bank Marketing Campaign Analysis

## Introduction
- Logistic regression is a widely-used classification algorithm primarily applied to predict the probability of a binary outcome. This analysis uses logistic regression to forecast client behavior, specifically to predict whether a client will subscribe to a term deposit. The model explores relationships between client demographics, past campaign performance, and subscription likelihood.

## Dataset Description
- The dataset used is the Bank Marketing Dataset from a marketing campaign conducted by a Portuguese financial institution. It includes details about client attributes, previous marketing campaigns, and whether the client subscribed to a term deposit.
  
- **Client-related features**:
  - `age`: The client's age.
  - `job`: Job type (categorical).
  - `marital`: Marital status (categorical).
  - `education`: Education level (ordinal).
  - `balance`: Account balance, indicating available savings.
  - `housing`: Whether the client has a housing loan (binary).
  - `loan`: Whether the client has a personal loan (binary).

- **Campaign-related features**:
  - `duration`: Duration of the last call in seconds (indicator of engagement).
  - `campaign`: Number of contacts made during the campaign.

- **Dependent Variable**:
  - `deposit` (target variable): Indicates if the client subscribed to a term deposit (`yes` or `no`).

## Objective
- The objective is to build a model that predicts whether a client will subscribe to a term deposit based on their attributes and previous campaign performance.

## Logistic Regression Analysis

### Data Preprocessing
1. **Handling Missing Values**:
   - Identify and manage missing data by using methods like mean, median, or advanced techniques such as K-nearest neighbors.
  <img alt = "Python" height="200" src="https://github.com/user-attachments/assets/28cd84d0-7ce0-4234-9d42-0d04c9b1729d">
    <img alt = "Python" height="300" src="https://github.com/user-attachments/assets/e70fe7a8-d691-45dc-976e-cce1b994af5a">
 </p>
 
###
2. **Label Encoding**:
   - Assign unique numbers to categorical variables:
     #### Job Categories
     The following numerical values have been assigned to the job categories:
     - **Student** = 1
     - **Unemployed** = 2
     - **Retired** = 3
     - **Housemaid** = 4
     - **Blue-collar** = 5
     - **Services** = 6
     - **Technician** = 7
     - **Admin.** = 8
     - **Self-employed** = 9
     - **Management** = 10
     - **Entrepreneur** = 11

     #### Marital Status
     The marital status categories are encoded as follows:
     - **Married** = 3
     - **Single** = 2
     - **Divorced** = 1
     #### Housing Status
     The housing status is represented by:
     - **Yes** = 1
     - **No** = 0
     #### Loan Status
     The loan status is encoded as:
     - **Yes** = 1
     - **No** = 0
     #### Deposit Subscription
     The deposit subscription status is represented by:
     - **Yes** = 1
     - **No** = 0

### Model Implementation
The following libraries are used:
- **Pandas** (`import pandas as pd`):
  - Data manipulation and analysis, especially for reading, inspecting, and cleaning the dataset.
  - **Functions**:
    - `pd.read_csv()`: Loads the dataset.
      ![image](https://github.com/user-attachments/assets/ef6abf66-757d-4efe-aa2d-d96913640c39)

    - `dataset.isnull()`: Checks for missing values.
      ![image](https://github.com/user-attachments/assets/b57f2a6f-7f7d-4c55-a61b-7b11be968ad0)

    - `fillna()`: Fills missing values.
      ![image](https://github.com/user-attachments/assets/6a16790c-6223-4bc7-947a-e12058cc4dbd)

    - `to_csv()`: Saves the cleaned dataset.
      ![image](https://github.com/user-attachments/assets/6af16652-28e1-46c1-888e-cd8cc132cff7)


- **Scikit-Learn**:
  - A machine learning library for preprocessing and modeling.
  - **Functions**:
    - `LabelEncoder`: Encodes categorical variables numerically.
      ![image](https://github.com/user-attachments/assets/0d86d4fa-d9a6-4d4c-a82f-f692367abd13)
       ![image](https://github.com/user-attachments/assets/d7aeaaa2-fc9a-471b-9e06-20e05c1c1e1d)

    - `train_test_split`: Splits the dataset into training and testing sets.
      ![image](https://github.com/user-attachments/assets/678a95ec-4f0e-43c0-8ce3-c9fe27ff7830)

    - `StandardScaler`: Standardizes input features.
      ![image](https://github.com/user-attachments/assets/88e2602c-0c62-4a34-ad6d-29bd22e6436f)

    - `LogisticRegression`: Provides the logistic regression model.
      ![image](https://github.com/user-attachments/assets/694106e0-e569-40a2-92d0-dc444851fa75)

    - `confusion_matrix`, `accuracy_score`: Calculates model accuracy and displays the confusion matrix.
      ![image](https://github.com/user-attachments/assets/8d85bc28-7f79-4376-923e-6e359f1827bd)
      ![image](https://github.com/user-attachments/assets/aa95a74d-06e5-4993-9750-a6063e7e9b0f)



- **Matplotlib** (`import matplotlib.pyplot as plt`):
  - For data visualization, particularly for displaying the confusion matrix.
- **Seaborn** (`import seaborn as sns`):
  - A visualization library for creating heatmaps to visualize the confusion matrix.
 ![image](https://github.com/user-attachments/assets/2aaf4344-1b71-4080-bdb4-ca6c72aa9b75)


### Making Predictions
- The model can make predictions on individual data points to assess whether a client is likely to subscribe to a term deposit.
![Screenshot 2024-10-31 072203](https://github.com/user-attachments/assets/936c7677-9cf1-42c5-9a5a-191c671d2b0c)
![Screenshot 2024-10-31 072407](https://github.com/user-attachments/assets/6d3464e7-0cda-4255-b68f-829510a19497)

## Results
### Model Evaluation
- **Confusion Matrix**: Helps identify false positives and false negatives, important for understanding model performance.
<img align="center" src="https://github.com/user-attachments/assets/7d50172a-17b5-4ced-86b2-b9fa02e12343">
</p>

### 
- **Accuracy Formula**:
  </p>
  
  ![Screenshot 2024-10-31 072741](https://github.com/user-attachments/assets/9bf3dead-3746-4dcf-9f9b-5bf388bd8753)
  </p>
  
  ![image](https://github.com/user-attachments/assets/dd87d3b4-3c98-444d-911c-30af3403822a)


- **Accuracy Score import from Sklearn**:
 ![Screenshot 2024-10-31 072828](https://github.com/user-attachments/assets/bf8d7bbb-b4e8-4260-a4de-9bec25a94ff9)
  - The model achieved an accuracy score of approximately 77.12%, indicating moderate effectiveness in predicting term deposit subscriptions.
 


## Discussion
- Logistic regression is relatively simple and highly interpretable. By examining the model coefficients, we can determine the influence of each feature on the likelihood of a client subscribing. This interpretability is valuable for understanding the relationship between client characteristics and campaign success.
    </p>
  With an accuracy of around 77.12%, the logistic regression model performs moderately well in predicting term deposit subscriptions. However, it has a noticeable rate of misclassification, specifically with false negatives. This can be a concern if the bank’s goal is to maximize subscription rates, as some clients who might subscribe could be missed by the model. Adjusting the model's focus depending on business priorities can enhance its effectiveness in distinguishing between clients likely to subscribe and those who are not.

## Datasets References

The datasets used in this project are available on Kaggle:

- [Salary Dataset on Kaggle](https://www.kaggle.com/datasets/mohithsairamreddy/salary-data)
- [Bank Marketing Dataset on Kaggle](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)





