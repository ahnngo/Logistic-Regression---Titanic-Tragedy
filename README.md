# Survival Chance - Titanic Tragedy: Project Overview 
* Created a machine learning model to predict what is the chance of a person of survive on the Titanic Tragedy
* Optimized Logistic Regression to generate good f-1 scores of 0.87 (0) and 0.76 (1)
* Deployed one-hot encoding to convert categorial data to numerical data

## Code and Resources Used 
**Python Version:** 3.10
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn
**Dataset:** https://www.kaggle.com/c/titanic 

## Data Cleaning
After creating a heatmap using seaborn, I figured out that age and cabin columns have a lot of missing values. 

![alt text](https://github.com/ahnngo/Logistic-Regression---Titanic-Tragedy/blob/main/Chart/Null%20value.png)

However, age has less missing value (around 20%) so I can still fill these out by create a box plot with Pclass with the logic that the older a person is, the more likely they can purchase more pricey ticket. 

![alt text](https://github.com/ahnngo/Logistic-Regression---Titanic-Tragedy/blob/main/Chart/Age%20vs%20Pclass%20Boxplot.png)

With the cabin column, since it has more than 70% null values, it does not say much or even decrease accuracy if I try to fill these null out. Therefore, I decided to drop this column.


## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![alt text](https://github.com/ahnngo/Logistic-Regression---Titanic-Tragedy/blob/main/Chart/Survided%20vs%20Pclass.png)

The more expensive their ticket were, the more likely they survived

![alt text](https://github.com/ahnngo/Logistic-Regression---Titanic-Tragedy/blob/main/Chart/Survided%20vs%20Sex.png)

Female had more chance to survive than male


## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 30%. I chose logistic regression model and it performs with good results. 

## Model performance

![alt text](https://github.com/ahnngo/Logistic-Regression---Titanic-Tragedy/blob/main/Chart/Screenshot%202022-04-20%20225240.png)


