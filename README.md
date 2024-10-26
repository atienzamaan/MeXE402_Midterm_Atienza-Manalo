 # MeXE402_Midterm_Atienza-Manalo
#### Both Linear Regression and Logistic Regression are foundational techniques in machine learning used for different types of problems. While they share similarities in their structure, they are applied to distinct tasks and have different mathematical foundations. This repository will serve as our midterm exam that is designed to assess our understanding of Linear Regression and Logistic Regression through practical application on real-world datasets.

# Linear Regression
# **Introduction**
# **Dataset Description**
This dataset contains information about salaries, years of experience, and other relevant factors. It's a suitable dataset for predicting salaries based on experience using linear regression.
#### **Key Features**:
  - `Salary`:The corresponding salary of the employee (in dollars).
  - `Years of Experience`: The number of years an employee has worked in their field.
  - `Gender:`The gender of the employee (e.g., Male, Female, Non-binary).
  - `Education Level:` The highest level of education attained by the employee (e.g., High School, Bachelor’s Degree, Master’s Degree, Ph.D.).
  - `Job title`: The employee's position or title within their organization (e.g., Software Engineer, Data Analyst, Project Manager).
  -  `Age:` The age of the employee (in years).
#### **Dependent Variable**:
   - `Salary`:The corresponding salary of the employee (in dollars).
# **Objective of the Dataset**
The objective of the Salary Dataset is to analyze the relationship between salaries and years of experience and to build predictive models using linear regression. The primary goal is to predict an individual's salary based on their years of experience and other relevant factors. This can help in understanding salary trends, making informed salary forecasts, and identifying patterns between experience and earnings.
# **Linear Regression Analysis**

## Data Preprocessing

### **1.	Handle Missing Values**
   
 <h2 align="center"> 
  
![image](https://github.com/user-attachments/assets/8c1a99fb-feb7-4fe8-b4cc-4e9c62596bb9)


<h2 align="center"> <small>FIGURE 1.1:Total number of missing values</small> </h2>
  
Figure 1.1 illustrates the initial step of the analysis, which involved utilizing Python to identify missing values within 6 columns of the Salary dataset. This figure showcases a series of missing numbers within these columns.

<h2 align="center"> 

![image](https://github.com/user-attachments/assets/035f86ca-7359-44c3-8cab-68a0474f6200)


</h2>



<h2 align="center"> <small>FIGURE 1.2:Row with Missing value</small> </h2>
 
  
Figure 1.2 shows the 6 rows that contain missing values across any of the columns. The analysis then determined the exact rows within the dataset where values were missing.


### **2. Dealing with missing data in your dataset**


>>2.1	Removing records with missing values.


<h2 align="center"> 
 
![image](https://github.com/user-attachments/assets/1aa758d8-4c13-4c9c-9622-d31812b1a981)


<h2 align="center"> <small>FIGURE 2.1:Removing Unnecessary Data</small> </h2>

Figure 2.1 codes ensure that any missing values (NaNs) in the six specified columns (Age, Gender, Educational Level, Job Title, Years of Experience, Salary) are replaced with the most common value (mode) for each column. This is a common technique when handling categorical or numerical data with missing values, where replacing missing data with the mode. It can help maintain the distribution of the dataset.

>>2.2 Saving the cleaned Dataset.

<h2 align="center"> 
 
![image](https://github.com/user-attachments/assets/93d7de5d-4fc6-4861-826c-156eb8cf82f8)

<h2 align="center"> 
 
![image](https://github.com/user-attachments/assets/053e362a-53d8-4e4a-ba68-5780666d63e9)

<h2 align="center"> <small>FIGURE 2.2:FILE LOCATION</small> </h2>

Figure 2.2 illustrates the steps taken to address missing data within the dataset. The final dataset, incorporating these changes, can be located in a folder named 'Documents/Projects'.

## **3. Converting categorical labels/text to numeric form.**

Label Encoder 
>A Label Encoder in scikit-learn is used to convert categorical labels (text or other non-numeric values) into numerical form. This is particularly useful in machine learning models, which generally require inputs to be in numeric form.


<h2 align="center"> 

![image](https://github.com/user-attachments/assets/38ae0f3b-27e0-415b-aaf8-d54d03bdf8ff)


![image](https://github.com/user-attachments/assets/f940fd7a-6575-4ea5-84b4-4a3dcc7f9a38)



<h2 align="center"> <small>FIGURE 3.1:Changing Variables to Numeric</small> </h2>


Figure 3.1 utilized a label encoder to replace all numeric values with non-numeric values, a requirement for linear regression.

Note: There was an issue with the Bachelor's degree data where the columns named "Bachelor's" from 1 to 1000 were equivalent to "0," and values 1001 and above were equivalent to "1." This was corrected using the Find and Replace method in Excel.


### **4. Map out the Excel file for easy reference, allowing you to understand what the numeric values represent**

<h2 align="center">

![image](https://github.com/user-attachments/assets/3a1ad860-ba16-40a2-a2c1-128bec2f79e0)


<h2 align="center"> <small>FIGURE 4.1:Reference Value</h2>


Figure 4.1 provides a comprehensive list of reference values associated with the numerical data used in the analysis. Due to the extensive nature of the dataset, containing 201 unique job titles, it is recommended to consult the accompanying Excel file named "Salary_Data_Reference_Value" for a detailed reference of numerical values. 

# **MODEL IMPLEMENTATION**:

1. 
<h2 align="center">

 
![image](https://github.com/user-attachments/assets/550a35c0-73dd-42b4-bf67-0038f6c0cf4b)


<h2 align="center"> <small>First, the panda’s library is imported as pd, which is a common convention. Then, the read_csv() function is used to load the CSV file named "Salary_Data_cleaned.csv" into a Pandas DataFrame named dataset. This Data Frame stores the data in a tabular format, making it easier to work with. Finally, the head () method is called on the dataset to display the first 5 rows of the DataFrame, providing a glimpse of the data's structure and content.</h2>


<h2 align="center">

![image](https://github.com/user-attachments/assets/b0ba06d9-6f78-4378-a43a-8e3b07c86352)

The code effectively separates the dataset into two parts:
-	X: Contains the independent variables (features) that will be used to predict the salary.
-	y: Contains the dependent variable (target) that represents the salary values to be predicted.
This step is crucial in machine learning workflows as it prepares the data for training a model.

<h2 align="center">

![image](https://github.com/user-attachments/assets/7d72a08e-f5c3-4fdf-b57c-1bd8e0cd36e6)


The train_test_split function is imported from the sklearn.model_selection module. This module provides various tools for model selection and evaluation. The train_test_split function is called with the input features (X), the target variable (y), the desired test set size (test_size=0.2), and a random seed (random_state=0). 


•  Output: The function returns four sets: 

•	X_train: Contains the features of the training set.

<h2 align="center">

![image](https://github.com/user-attachments/assets/cca04608-22b3-435b-abf6-9f9749440f1c)


•	X_test: Contains the features of the testing set.

<h2 align="center">

![image](https://github.com/user-attachments/assets/7622d195-4ca6-4339-bb65-4773e1dc2ab9)

•	y_train: Contains the target variable of the training set.

<h2 align="center">

![image](https://github.com/user-attachments/assets/7784ec50-d46c-4603-82ed-662fe2edb120)


•	y_test: Contains the target variable of the testing set.

<h2 align="center">

![image](https://github.com/user-attachments/assets/8ad4cf68-60ec-4584-a084-f9c22ff7daf3)


![image](https://github.com/user-attachments/assets/66bb8180-9615-4fa0-b227-d51f6929f2a1)


This class provides a pre-built implementation of the linear regression algorithm. By creating an instance of this class, we effectively instantiate a linear regression model object. This model is now ready to be trained on the training data


<h2 align="center">

![image](https://github.com/user-attachments/assets/99926d4e-bd5a-4de1-a547-a5ecf2f23af5)

This line of code trains the linear regression model (model) on the training data. The fit method is like a function that takes the training features (X_train) and the corresponding target variable (y_train) as input. It teaches the model the best way to relate the features to the target.


<h2 align="center">
 
![image](https://github.com/user-attachments/assets/8d3f4c14-6868-42c6-8c7e-03a4719aff1c)

This line of code uses the trained model (model) to make predictions on the testing set (X_test). The predict method takes the input features of the testing set as input and returns the corresponding predicted target values. These predicted values are stored in the variable y_pred. 


<h2 align="center">

![image](https://github.com/user-attachments/assets/d8f6bad8-f5cb-4b84-bf87-0f263ab81a22)

![image](https://github.com/user-attachments/assets/ab59761b-dd77-4c7e-929c-5c5a5add3072)


•  This line of code uses the trained model (model) to make a prediction on a new data point. The input to the predict method is a 2D array containing the values for the input features of the new data point. In this case, the values are: age = 32, gender = 1, education level = 1, job title = 177, and years of experience = 5. 

•  Output: The predict method returns a predicted value, which in this case is 85745.79735184. This predicted value represents the estimated salary for the given data point based on the model's learned relationship between the input features and the target variable.

<h2 align="center">

![image](https://github.com/user-attachments/assets/23090e2d-4be9-42d6-b0cd-8bfcbee148b3)



This refers to using appropriate machine learning libraries to build and train the linear regression model. Commonly used libraries include:

- o	Scikit-learn for linear regression.
- o	Pandas and Numpy for data handling.
- o	Label Encoder for transforming categorical labels into numerical values.

Evaluation Metrics:
- 	Calculate R-squared
-  Mean Squared Error


## **The Significance of Coefficients in the Salary Dataset**:

The coefficients in a salary dataset provide valuable insights into which factors are most influential in predicting salary. They help identify patterns like gender pay gaps, the impact of education, and the value of experience, which can guide decisions related to compensation strategies, hiring practices, and addressing potential salary disparities. Here are the importance of coefficient under: 

#### **Age**:

The coefficient for age indicates how salary is expected to change with each additional year of age. In this dataset, it suggests that older individuals tend to earn more, likely due to the accumulation of experience or seniority.

#### **Gender**:

The gender coefficient measures the salary difference between males and females. In this dataset, there is no strong evidence of a significant gender-based salary gap.

#### **Education Levelt**:


The coefficient for education level reflects how salary is affected by increasing educational attainment. Individuals with higher levels of education tend to earn more, supporting the idea that education boosts earning potential.

#### **Job Title**:


This coefficient reflects salary differences across various roles. It indicates that certain job titles command higher or lower salaries, depending on the position's value in the job market.


#### **Years of Experience**:
Experience is one of the most critical factors. The coefficient for years of experience suggests that salary tends to increase with each additional year showing the rate of salary growth.



## **Model’s Predictive Power**:

The predictive power of your model can be assessed using metrics like R-squared (R²), Adjusted R-squared, and error measures. 

## **Key Metrics**:

1.	R-squared (R²): 0.6617
   
- R² explains how well the independent variables account for the variance in the dependent variable (salary).
- 66.17% of the variability in salary is explained by the model. This is moderately good, suggesting that your model captures most but not all of the salary determinants.

2.	Adjusted R-squared: 0.6603
- Adjusted R² adjusts for the number of predictors in the model. It penalizes the inclusion of irrelevant predictors that don't contribute to the model's predictive power.
- 66.03% means that even after accounting for the complexity of the model (number of predictors), the model still explains most of the variance in salary. The slight decrease from R² indicates that the model isn’t overfitting, as the number of predictors is appropriate.
  
Model Performance:

•	The R² and Adjusted R² values around 66% imply that your model has a moderate predictive power. While the model captures a large part of the variability in salary, there's still about 34% that remains unexplained. This could be due to other factors not included in the model, such as industry type, company size, performance incentives, or even location.

------

## Logistic Regression 
### **Introduction**
#### **Dataset Description**
##### The dataset used in this analysis is the **Bank Marketing Dataset** from a marketing campaign conducted by a Portuguese financial institution. The dataset contains information on client attributes, previous marketing campaign details, and whether the client subscribed to a term deposit.

#### **Key Features**:
- **Client-related features**:
  - `age`: The age of the client.
  - `job`: The type of job the client has (categorical).
  - `marital`: The client’s marital status (categorical).
  - `education`: The client’s level of education (ordinal).
  
- **Campaign-related features**:
  - `contact`: The type of communication used during the campaign.
  - `previous`: Number of contacts performed before this campaign.
  
- **Output**:
  - `y`: The target variable indicating whether the client subscribed to a term deposit (`yes` or `no`).

### **Objective of the Dataset**:
The objective is to build a model to predict whether a client will subscribe to a term deposit based on the client’s attributes and the previous campaign's performance.

---




##### Explanation
![image](https://github.com/user-attachments/assets/be9096cd-e27a-44e2-b681-33ca4e35f352)
##### Project Objectives:
