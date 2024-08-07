# Machine-Learning-Model-Prediction
 ## Boston House Price Prediction


## Resources
Python script boston_houseing.py for analysis
Results figure saved in plots folder
Dockerfile for running the script in any operating system
RUNME.md for guiding to run the python script
## Research Question
What is the best Model for predicting Boston house prices?

## Abstract
Opportunity: Data was collected from a real survay
Challenge: Data was collected in 1078, only 506 entries and 14 features
Action: Statistical analysis and Machine Learning models will be utilized to get the answer
Resolution: I will find the best ML model to predict the house prices
## Introduction
Boston House Prices Dataset (Source: https://scikit-learn.org/stable/datasets/index.html#toy-datasets) is used for the research.

This data was collected in 1978 and has 506 entries with 14 attributes or features for homes from various suburbs in Boston.

Boston Housing Dataset Attribute Information (in order):
        - CRIM     per capita crime rate by town
        - ZN       proportion of residential land zoned for lots over 25,000 sq.ft.
        - INDUS    proportion of non-retail business acres per town
        - CHAS     Charles River dummy variable (= 1 if tract bounds river; 0 otherwise)
        - NOX      nitric oxides concentration (parts per 10 million)
        - RM       average number of rooms per dwelling
        - AGE      proportion of owner-occupied units built prior to 1940
        - DIS      weighted distances to five Boston employment centres
        - RAD      index of accessibility to radial highways
        - TAX      full-value property-tax rate per $10,000
        - PTRATIO  pupil-teacher ratio by town
        - B        1000(Bk - 0.63)^2 where Bk is the proportion of blacks by town
        - LSTAT    % lower status of the population
        - MEDV     Median value of owner-occupied homes in $1000's
## Methods
Following steps have been performed to get the answer of my research question.

Step 1: Choose the tool and technology for doing the research.

Step 2: Get the data

Step 3: Process data for analysis

Step 4: Perform exploratory data analysis and find the important variables

Step 5: Prepare Training & Test dataset

Step 6: Create Models for predicting price and perform testing

Step 7: Measure performance of the Models and choose best Model

## Results
Exploratory Data Analysis (EDA)
I have used some visualizations to understand the relationship of the target variable MEDV with other features. First plot is the distribution of the target variable MEDV. I have used the distplot function from the seaborn library. alt text

We see that the values of MEDV are distributed normally with few outliers.

Next, I have created a correlation matrix that measures the linear relationships between the variables. The correlation matrix is formed by using the corr function from the pandas dataframe library. I have also used the heatmap function from the seaborn library to plot the correlation matrix.


The correlation coefficient ranges from -1 to 1. If the value is close to 1, it means that there is a strong positive correlation between the two variables. When it is close to -1, the variables have a strong negative correlation.

By looking at the correlation matrix we can see that RM has a strong positive correlation with MEDV (0.7) and LSTAT has a high negative correlation with MEDV (-0.74).

Finally I have created scatter plots to see correlate among MEDV, RM and LSTAT. I have used the scatterplot function from the seaborn library.

From the scatter plots we can see that the MEDV or prices increase as the value of RM increases linearly. There are few outliers and the data seems to be capped at 50. And the prices tend to decrease with an increase in LSTAT.

Based on the above observations I have taken independent feature RM and LSTAT to predict dependent feature MEDV or Price.

# Model Creation and Testing
I have created three models with following regressors and evaluate the Mean Squared Error (MAE) and Mean Accuracy Error (MAE) of each of them with train-test split (80-20) dataset.

Linear Regression
