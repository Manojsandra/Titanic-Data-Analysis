## Titanic-Data-Analysis
Performed exploratory data analysis, feature engineering, and visualization on the Titanic dataset to identify patterns affecting passenger survival.

## Project Title
Titanic Exploratory Data Analysis

## Objective
The goal of this project is to perform exploratory data analysis (EDA) on the Titanic dataset to identify patterns and factors that influenced passenger survival.

## Dataset Information
# Dataset
The dataset contains passenger details such as age, sex, passenger class,name,sibsp,parch, fare, family information,cabin,Embarked and survival status from the Titanic disaster.

## Dataset
The dataset used in this project is the Titanic dataset from Kaggle:
https://www.kaggle.com/competitions/titanic/data
## Data Cleaning
During the data cleaning process, I identified missing values in the Age, Cabin, and Embarked columns.

.The Age column contained several missing values. Since age is numerical data, I replaced the missing values using the mean of the column.
.The Embarked column is categorical data and had a few missing values, so I filled them using the mode (most frequent value).
.The Cabin column had more than 50% missing values, which could affect the analysis. Therefore, I decided to drop the column from the dataset.

Additionally, I noticed that the Age column was stored as a float data type. Since age values are generally represented as whole numbers, I converted the Age column from float to integer.


