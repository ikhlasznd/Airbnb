# Airbnb
Airbnb_project


# Table of Contents:

### - Installation

### - Project Motivation

### - File Descriptions

### - CRISP-DM process

### - Kernel Notebook 

### - Results


## Installation:
There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3.*


## Project Motivation:

In this project, I was interestested in using Seattle Airbnb Dataset from Kaggle to better understand:

1- What is the Seattle neighbourhood that has houses with higher prices?

2- What is the Seattle neighbourhood that has houses with the cheapest prices?

3- Which type of properties is the most expensive in Seattle?


## File Descriptions:

This file contains a notebook in which the entire analysis process is shown. There is also a listings.csv that contains the data used to answer the above questions. 

## CRISP-DM process:

### 1- Understanding the business

 In this project, I was interested mainly to determine the features that could define the general prices of houses in Airb&B in order to develop a machine learning model that could easily determine the price of a given houses according to those features. however, before that, it was also beneficial to get an idea about: 

* 1- What is the Seattle neighbourhood that has houses with higher prices?

* 2- What is the Seattle neighbourhood that has houses with the cheapest prices?

* 3- Which type of properties is the most expensive in Seattle


### 2- Understanding the data

 The data that will be used to answer the above question is a dataset of different houses that could be found in Airb&b in the area of Seattle. The dataset is constituted of 92 which means that we have approximately 92 features of houses, and 3818 rows which means that there are 3818 house registered in this dataset. 
 
 
### 3- Preparation of data

After getting a general idea about the data that we have, we will process in cleaning the columns that we will need in the analysis especially that many columns are not in a good format. After that, we will use the Pearson Correlation to determine which features are correlated the most with the "price". 


### 4-Modelling

After getting a list of columns(features) that are the most correlated with the price, we will implement a K-Neighbours Regressor algorithm on both of the two datasets. A K nearest neighbours is a simple algorithm that stores all available cases and predict the numerical target based on a similarity measure (e.g., distance functions)(1).

For that purpose, we will split our data into train and test parts. Then, we will choose the default value of Number of neighbours to use by default for neighbours queries which is 5 and a "brute" algorithm that will use a brute-force search.

(1) https://www.saedsayad.com/k_nearest_neighbors_reg.htm#:~:text=K%20nearest%20neighbors%20is%20a,as%20a%20non-parametric%20technique.


### 5- Evaluation

We will evaluate the accuracy of each model to determine which one of the two scenarios has done the best price predictions. For that, we will use the Mean Squared Error which is a measure of how close a fitted line is to data points and the Root Mean Square Error which is just the square root of the mean square error and is directly interpretable in terms of measurement units. 


### 6- DEPLOYMENT

In this project, we were interested in knowing which features determine the price of a house in Airb&b. For that, we have stimulated two scenarios: 

In the first one, we have manually chosen a subset of features that we thought they influenced the most the houses price in Airbnb. Those features were: accommodates, bedrooms, bathrooms, minimum nights, maximum nights and the number of reviews.

In the second one, we have done a features selection using the Filter method. The features chosen by this method were: accommodates, bathrooms, bedrooms, beds. Those features  have a strong correlation with the price.

We have then implemented K-Neighbours Regressor algorithm to predict the houses prices and evaluated the models using the  Mean Squared Error and the Root Mean Square Error. 

The result of the evaluation shows  the second scenario has performed the best price prediction as the MSE and RMSE were the lowest one, that means the features selected by the Filter method were more appropriate to predict the houses prices.



## Kernel Notebook 

https://www.kaggle.com/ikhlaszineddine2103/airbnb-project

## Results
The main findings of the code can be found at the post available [Medium Post](https://medium.com/dev-genius/features-selection-importance-in-machine-learning-for-a-better-prediction-of-business-patterns-aa9ee7fa2785)









