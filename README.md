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

1.The Age column contained several missing values. Since age is numerical data, I replaced the missing values using the mean of the column.

2.The Embarked column is categorical data and had a few missing values, so I filled them using the mode (most frequent value).

3.The Cabin column had more than 50% missing values, which could affect the analysis. Therefore, I decided to drop the column from the dataset.

Additionally, I noticed that the Age column was stored as a float data type. Since age values are generally represented as whole numbers, I converted the Age column from float to integer.

## EDA 
## 1.UNIVARIATE ANALYSIS
Age Feature Analysis

I performed univariate analysis on the Age feature using a histogram and density plot to understand the distribution of passenger ages.

Observations:
The age distribution is slightly right-skewed.
The highest concentration of passengers is between 25 and 30 years of age.
This indicates that most passengers traveling on the Titanic were young adults.
There are fewer passengers at higher age ranges (above 60 years).
Some very young passengers (children) are also present in the dataset.

## Age Boxplot Analysis

To identify outliers in the Age feature, I used a box plot.

The box plot shows that most passengers were between 20 and 35 years old, with a median age around 28 years. Some passengers with ages above 55 appear as outliers because they are far from the majority of the data distribution.

These outliers were not removed because they represent valid passenger ages and are important for analysis.
