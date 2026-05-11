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

1.The Age column contained several missing values. Since age is numerical data, I replaced the missing values using the mean of the column.<br>2.The Embarked column is categorical data and had a few missing values, so I filled them using the mode (most frequent value).<br>
3.The Cabin column had more than 50% missing values, which could affect the analysis. Therefore, I decided to drop the column from the dataset.

Additionally, I noticed that the Age column was stored as a float data type. Since age values are generally represented as whole numbers, I converted the Age column from float to integer.

## EDA 
## 1.UNIVARIATE ANALYSIS
### Age Feature Analysis

I performed univariate analysis on the Age feature using a histogram and density plot to understand the distribution of passenger ages.

#### Observations:
The age distribution is slightly right-skewed.
The highest concentration of passengers is between 25 and 30 years of age.
This indicates that most passengers traveling on the Titanic were young adults.
There are fewer passengers at higher age ranges (above 60 years).
Some very young passengers (children) are also present in the dataset.

## Age Boxplot Analysis

To identify outliers in the Age feature, I used a box plot.

The box plot shows that most passengers were between 20 and 35 years old, with a median age around 28 years. Some passengers with ages above 55 appear as outliers because they are far from the majority of the data distribution.

These outliers were not removed because they represent valid passenger ages and are important for analysis.

## Fare Feature Analysis
I performed univariate analysis on the Fare feature using a histogram and density plot to understand the distribution of passenger ages.

#### Observations
The Fare distribution is highly right-skewed.<br>
Most ticket prices are concentrated between 0 and 50.<br>
This indicates that the majority of passengers purchased lower-priced tickets.<br>
Since lower ticket fares are generally associated with Third Class (Pclass = 3) passengers, it suggests that most passengers belonged to the third class.<br>
Only a small number of passengers purchased high-priced tickets, which represents passengers from higher classes.

#### Conclusion
The fare distribution shows that the Titanic carried more lower-class passengers compared to upper-class passengers.

## 2.UNIVARIATE ANALYSIS FOR CATEGORICAL DATA
#### Survival Feature Analysis

I performed univariate analysis on the Survived feature using a count plot to understand the survival distribution of passengers

#### Observations
The dataset shows that a larger number of passengers did not survive.<br>
Around 549 passengers died, while approximately 342 passengers survived.<br>
This indicates that the survival rate on the Titanic was relatively low.<br>

#### Conclusion
The Survived feature is imbalanced because the number of non-survivors is greater than the number of survivors.

## Passenger Class (Pclass) Analysis
I performed univariate analysis on the Pclass feature to understand the distribution of passengers across different ticket classes.

#### Observations
Most passengers belonged to Class 3.<br>
Around 491 passengers traveled in Class 3.<br>
Around 216 passengers belonged to Class 1.<br>
Around 184 passengers belonged to Class 2.<br>
This confirms the earlier observation from the Fare analysis that the Titanic carried more lower-class passengers.

#### Conclusion
The dataset shows that the majority of passengers were from the third class, while fewer passengers traveled in first and second classes.

## Sex Feature Analysis
I performed univariate analysis on the Sex feature to understand the gender distribution of passengers on the Titanic.

#### Observations
The number of male passengers was significantly higher than female passengers.<br>
Around 577 passengers were male.<br>
Around 314 passengers were female.<br>
This indicates that most passengers traveling on the Titanic were men.<br>

#### Conclusion
The dataset contains a higher proportion of male passengers compared to female passengers.

## SibSp Feature Analysis
I performed univariate analysis on the SibSp feature to understand how many passengers were traveling alone or with siblings/spouses.

#### Observations
Most passengers were traveling alone.<br>
Around 608 passengers had SibSp = 0, meaning they were not traveling with siblings or spouses.<br>
Around 209 passengers had SibSp = 1.<br>
Smaller numbers of passengers traveled with larger family groups:<br>
SibSp = 2 → 28 passengers<br>
SibSp = 3 → 16 passengers<br>
SibSp = 5 → 5 passengers<br>
SibSp = 8 → 7 passengers<br>

#### Conclusion
The analysis shows that the majority of Titanic passengers traveled alone, while fewer passengers traveled with family members.

## Parch Feature Analysis
I performed univariate analysis on the Parch feature to understand how many passengers were traveling with parents or children.

#### Observations
Most passengers were traveling without parents or children.
Around 678 passengers had Parch = 0, indicating they were traveling alone in terms of parent-child relationships.
Around 118 passengers had Parch = 1.
Around 80 passengers had Parch = 2.
Very few passengers traveled in larger family groups:
Parch = 3 → 5 passengers
Parch = 4 → 4 passengers
Parch = 5 → 5 passengers
Parch = 6 → 1 passenger

#### Conclusion
The analysis shows that most passengers were not traveling with parents or children, indicating that solo travel was more common on the Titanic.

# BIVARIATE ANALYSIS
