# Black Friday Sales Prediction Analysis

This project aims to predict the total purchase amount made by customers during the Black Friday sale event at a retail store. The dataset includes various customer-related and product-related features that can be used to predict the amount a customer will spend. The goal is to build a regression model that can predict the `Purchase` amount based on these features.

## Problem Statement

The objective of this project is to predict the `Purchase` amount of a customer during the Black Friday sale. We use various features, including customer demographics (age, gender, occupation, etc.) and product-related details, to build a machine learning model.

## Dataset Information

The dataset consists of **550,069 rows** and **12 columns**, with the following attributes:

| Column ID | Column Name                     | Data Type  | Description                                                                 | Masked |
|-----------|----------------------------------|------------|-----------------------------------------------------------------------------|--------|
| 0         | User_ID                          | int64      | Unique ID of the customer                                                   | False  |
| 1         | Product_ID                       | object     | Unique ID of the product                                                     | False  |
| 2         | Gender                           | object     | Gender of the customer                                                       | False  |
| 3         | Age                              | object     | Age of the customer                                                           | False  |
| 4         | Occupation                       | int64      | Occupation code of the customer                                              | True   |
| 5         | City_Category                    | object     | City category of the customer                                                | True   |
| 6         | Stay_In_Current_City_Years       | object     | Number of years the customer has stayed in the current city                 | False  |
| 7         | Marital_Status                   | int64      | Marital status of the customer                                               | False  |
| 8         | Product_Category_1               | int64      | Category of the product                                                      | True   |
| 9         | Product_Category_2               | float64    | Category of the product (with missing values)                                | True   |
| 10        | Product_Category_3               | float64    | Category of the product (with missing values)                                | True   |
| 11        | Purchase                         | int64      | Amount the customer spent during Black Friday sale                           | False  |

## Steps Followed

### 1. **Exploratory Data Analysis (EDA)**

Exploratory Data Analysis (EDA) was conducted to gain insights into the data. The distribution of the target variable `Purchase` was visualized, and various plots were created for features like Gender, Age, Marital Status, and others to understand the data better.

### 2. **Data Preprocessing**

- **Handling Missing Data**: Missing values in the columns `Product_Category_2` and `Product_Category_3` were filled with a placeholder value `-2.0`.
- **Encoding Categorical Features**: Categorical features like `Gender`, `Age`, `City_Category`, and `Stay_In_Current_City_Years` were encoded to numeric values to make them suitable for machine learning models.

### 3. **Model Training**

Various machine learning models were trained to predict the `Purchase` amount, including:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Extra Trees Regressor**

### 4. **Model Evaluation**

Models were evaluated using **Mean Squared Error (MSE)** and **Cross-Validation (CV) Score**. The goal was to minimize these metrics to get the best prediction performance.

### 5. **Final Results**

- **Linear Regression**: 
  - MSE: 4617.99
  - CV Score: 4625.25
  
- **Decision Tree Regressor**: 
  - MSE: 3366.97
  - CV Score: 3338.59
  
- **Random Forest Regressor** (Best Model): 
  - MSE: 3062.66
  - CV Score: 3052.78
  
- **Extra Trees Regressor**:
  - MSE: 3194.07
  - CV Score: 3180.55

## Verdict

The **Random Forest Regressor** model achieved the best performance in terms of both MSE and CV Score, suggesting that it was the most accurate model for predicting purchase amounts. 

The project involved thorough data exploration, preprocessing, and evaluation of various machine learning models. The best performing model, Random Forest Regressor, showed promising results for predicting purchase amounts on Black Friday based on customer demographics and product information.

## Conclusion

- **Best Model**: Random Forest Regressor
- **Next Steps**: Further tuning of the Random Forest model (e.g., hyperparameter optimization) could potentially improve the performance even more.

