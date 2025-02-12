# Laptop Price Prediction

## Overview
The Laptop Price Prediction project aims to accurately predict laptop prices based on their features. Our process includes data pre-processing, feature engineering, and encoding. We then select and train models to provide precise price predictions. Finally, we deploy the model for organizations to estimate laptop prices based on specific specifications.

## Problem Statement
Predicting the accurate price of laptops is crucial for maintaining an organization's reputation and credibility. Any misconceptions or errors in price prediction can significantly impact the organization. This project focuses on learning from data to create a robust and accurate model that predicts laptop prices with minimal errors.

## Requirements
 - Python
 - Pandas
 - Matplotlib/Seaborn
 - Scikit-learn (sklearn)

## Methodology

  ### Data Preprocessing
   - We start by addressing any missing or null values in our dataset, ensuring they are handled appropriately using suitable methods.
   - For numerical columns, we fill the missing values with the **mean** of the column using the **fillna** method.
   - To detect outliers, we create boxplots. Apart from the **Price** column, we don't have many outliers in our data.

  ### Exploratory Data Analysis(EDA)
   - **EDA** helps us better understand the relationships between different data columns, which is useful for feature selection.We create visualizations such as histograms and scatter plots using the **Matplotlib** library.
   - We calculate numerical metrics like mean and median, and visualize correlations between columns using **heatmaps**.

  ### Encoding Categorical Data
   - Models cannot directly use non-numeric (categorical) data for training, so we need to encode these columns. We use **LabelEncoder** for this purpose.
   - To save time and space, we encode all categorical columns in a single run using an encoder variable and the **apply()** method, instead of manually encoding each column.

  ### Feature Engineering and Selection
   - In this step, we identify the important features that will be used for model training. This involves analyzing the dataset to understand which features 
     are most relevant to predicting the target variable.
   - We split the data into features (x) and the target variable (y). The features represent the input data, while the target variable represents the 
     output we want to predict.

  ### Split The Data
   - For split the data in training and testing part we employ **train_test_split** for that and store this in variables like **x_train, y_train, x_test, y_test** according to the percentage of distribution.
   - Normally, here we use the train_size is 80% of whole data and the **random_state** which makes the stable output is set to **42**.

  ### Train and Evaluate Model Performance
   - After spliting and other operation now the time is to train the model where here we choose it after verifying the score from **KFold** and **cross_val_score** techniques.
   - Where we got that a model named **RandomForestRegressor** is best for our data and after using **best estimators** we achieved the score of **81%** while testing which is good score for our model. 

## Results
 - As a result, we have developed a robust predictive model for estimating laptop prices with a low mean error. Our model achieved a performance score of over **80%** during testing, meaning it accurately predicted prices for **80 out of 100** samples.
 - Organizations can leverage this model for future price predictions. For example, during sales or promotions, they can reduce the prices of high-demand laptops with attractive features to optimize sales and meet customer needs.

## Conclusion
In conclusion, the regressor model created using the **RandomForestRegressor** algorithm effectively handles future/input data provided by the user. Based on the training, it accurately predicts the laptop price according to the given feature values. Organizations need to understand the required input features for making predictions, allowing them to obtain reliable laptop prices based on these features. 
