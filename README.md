
# Predicting home prices - (Data Science and Machine Learning Model) 
## INTRODUCTION 

In this project, we will develop and evaluate the performance and the predictive power of a model trained and tested on data collected from houses in the Bangalore suburbs.
Once we get a good fit, we will use this model to predict the monetary value of a house located in the Bangalore area.
A model like this would be very valuable for a real state agent who could make use of the information provided on a daily basis.

## Objective and data - 
The goal is to predict sale prices for homes in Bangalore, India. You’re given a training and testing data set in CSV format as well as a data dictionary.

Training: Our training data consists of 5800 examples of houses with 244 features describing every aspect of the house. We are given sale prices (labels) for each house. The training data is what we will use to “teach” our models.

Testing: The test data set consists of 1,451 examples with the same number of features as the training data. Our test data set excludes the sale price because this is what we are trying to predict. Once our models have been built we will run the best one in the test data.

#### Task:
Machine learning tasks are usually split into three categories; supervised, unsupervised, and reinforcement. our task is supervised learning.
Supervised learning uses examples and labels to find patterns in data
It’s easy to recognize the type of machine learning task in front of you from the data you have and your objective. We’ve been given housing data consisting of features and labels, and we’re tasked with predicting the labels for houses outside of our training data.
Tools
I used Python and Jupyter notebooks for the competition. Jupyter notebooks are popular among data scientists because they are easy to follow and show your working steps.
Libraries: These are frameworks in python to handle commonly required tasks. I Implore any 
budding data scientists to familiarise themselves with these libraries:

Pandas — For handling structured data  
Scikit Learn — For machine learning   
NumPy — For linear algebra and mathematics



## Project Pipeline
Generally speaking, machine learning projects follow the same process. Data ingestion, data cleaning, exploratory data analysis, feature engineering, and finally machine learning.
The pipeline is not linear and you might find you have to jump back and forth between different stages. It’s important I mention this because tutorials often make you believe the process is much cleaner than in reality.

## Data Cleaning   
Kaggle does its best to provide users with clean data. However, we mustn’t become lazy, there are always surprises in the data.

#### Duplicates & NaNs:                           
I started by removing duplicates from the data and checked for missing or NaN (not a number) values. It’s important to check for NaNs (and not just because it’s socially moral) because these cause errors in the machine learning models.

#### Categorical Features:    
There are a lot of categorical variables that are marked as N/A when a feature of the house is nonexistent. For example, when no size is present. I identified all the cases where this was happening across the training and test data and replaced the N/As with something more descriptive. N/As can cause errors with machine learning later down the line so get rid of them.

#### Date Features:   
For this exercise, dates would be better used as categories and not integers. After all, it’s not so much the magnitude that we care about but rather that the dates represent different years. Solving this problem is simple, just convert the numeric dates to strings.
Decoded Variables: Some categorical variables had been number encoded.
The machine learning algorithm could interpret the magnitude of the number to be important rather than just interpreting it as different categories of a feature. To solve the problem, I reverse engineered the categories and recoded them.

## Exploratory Data Analysis (EDA)
This is where our data visualization journey often begins. The purpose of EDA in machine learning is to explore the quality of our data. A question to keep in mind is; are there any strange patterns that leave us scratching our heads?

## Feature Engineering

Machine learning models can’t understand categorical data. Therefore we will need to apply transformations to convert the categories into numbers. The best practice for doing this is via one hot encoding.
OneHotEncoder solves this problem with the options that can be set for categories and handling unknowns. It’s slightly harder to use but definitely necessary for machine learning.

## Machine learning
I follow a standard development cycle for machine learning. As a beginner or even a pro, you’ll likely have to go through many iterations of the cycle before you are able to get your models working to a high standard.

Therefore, I approached this problem with three machine learning models. Decision tree, Linear Regression, and Lasso boosting machines. This approach saves a lot of time as decision trees are quick to train and can give you an idea of how to tune the hyperparameters for my candidate models.
Model mechanics: I will not go into too much detail about how each model works here. Instead, I’ll drop a one-liner and link you to articles that describe what they do “under the hood”.

#### Decision Tree — 
A tree algorithm used in machine learning to find patterns in data by learning decision rules.

#### Linear model —   
Linear models describe a continuous response variable as a function of one or more predictor variables. They can help you understand and predict the behavior of complex systems or analyze experimental, financial, and biological data. Linear regression is a statistical method used to create a linear model.


#### Lasso Model —  
LASSO, short for Least Absolute Shrinkage and Selection Operator, is a statistical formula whose main purpose is the feature selection and regularization of data models.


# Training
Machine learning training refers to the process of teaching your model using examples from your training data set. In the training stage, you’ll tune your model hyperparameters.

#### Model Bias -
 Models that underfit the training data leading to poor predictive capacity on unseen data. Generally, the simpler the model the higher the bias.

#### Model Variance -  
Models that overfit the training data leading to poor predictive capacity on unseen data. Generally, the more complexity in the model the higher the variance.


# Result - 
As Result Linear Model is Best sored with ~82%. And Lasso and Decision Tree with ~ 69% of accuracy.
