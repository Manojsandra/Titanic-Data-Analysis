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
Most passengers were traveling without parents or children.<br>
Around 678 passengers had Parch = 0, indicating they were traveling alone in terms of parent-child relationships.<br>
Around 118 passengers had Parch = 1.<br>
Around 80 passengers had Parch = 2.<br>
Very few passengers traveled in larger family groups:<br>
Parch = 3 → 5 passengers<br>
Parch = 4 → 4 passengers<br>
Parch = 5 → 5 passengers<br>
Parch = 6 → 1 passenger<br>

#### Conclusion
The analysis shows that most passengers were not traveling with parents or children, indicating that solo travel was more common on the Titanic.

## 3.BIVARIATE ANALYSIS
## Pclass vs Survived Analysis
I performed bivariate analysis between Pclass and Survived to understand how passenger class affected survival chances.

#### Observations
In Class 1, most passengers survived.<br>
Survived: 136<br>
Not Survived: 80<br>
In Class 2, the number of survivors and non-survivors was relatively close.<br>
Survived: 87<br>
Not Survived: 97<br>
In Class 3, most passengers did not survive.<br>
Survived: 119<br>
Not Survived: 372<br>

#### Conclusion
Passenger class had a strong impact on survival rates. First-class passengers had a higher chance of survival, while third-class passengers experienced the highest number of deaths.

## Sex vs Survived Analysis
I performed bivariate analysis between Sex and Survived to understand how gender affected survival rates on the Titanic.

#### Observations
Female passengers had a much higher survival rate compared to male passengers.<br>
Female Survived: 233<br>
Female Not Survived: 81<br>
Most male passengers did not survive.<br>
Male Survived: 109<br>
Male Not Survived: 468<br>

#### Conclusion
Gender had a significant impact on survival. Female passengers were more likely to survive, while the majority of male passengers died during the disaster.
 
## Age vs Survived Analysis
I performed bivariate analysis between Age and Survived to understand how age affected survival.

#### Observations
The average age of passengers who did not survive was approximately 30.24 years.
The average age of passengers who survived was approximately 28.43 years.
This indicates that slightly younger passengers had a higher survival rate compared to older passengers.

#### Conclusion
There is only a small difference between the average ages of survivors and non-survivors. However, survivors were slightly younger on average.

## KDE Analysis for Age vs Survived
To better understand the relationship between Age and Survived, I used a KDE (Kernel Density Estimation) plot to compare the age distribution of survivors and non-survivors.

#### Observations
The KDE plot shows that many children had a higher chance of survival.<br>
In the age group between 20 and 40 years, a larger number of passengers did not survive.<br>
The density curve for non-survivors is higher in this range compared to survivors.<br>
Survival rates decrease for some adult age groups, especially among male passengers.<br>

#### Conclusion
The analysis indicates that children were more likely to survive, while many passengers between 20 and 40 years old did not survive during the disaster.

## SibSp vs Survived Analysis
I performed bivariate analysis between SibSp and Survived to understand how traveling with siblings or spouses affected survival chances.

#### Observations
Passengers traveling alone (SibSp = 0) had a lower survival rate compared to passengers traveling with small families.<br>
Passengers with SibSp = 1 had a better chance of survival.<br>
Passengers with small family sizes such as 1 or 2 siblings/spouses showed relatively higher survival rates.<br>
As the SibSp value increased, the survival rate generally decreased.<br>
Very large family groups had lower chances of survival.<br>

#### Conclusion
The analysis suggests that passengers traveling with small families had better survival chances compared to passengers traveling alone or with very large families.

## Embarked vs Survived Analysis
I performed bivariate analysis between Embarked and Survived to understand how the port of embarkation affected survival rates.

#### Observations
Southampton (S)<br>
Total passengers: 646<br>
Not Survived: 427<br>
Survived: 219<br>
Most passengers boarded from Southampton, and a large number of them did not survive.

Cherbourg (C)<br>
Total passengers: 168<br>
Not Survived: 75<br>
Survived: 93<br>
Passengers from Cherbourg had a relatively higher survival rate compared to Southampton passengers.

Queenstown (Q)<br>
Total passengers: 77<br>
Not Survived: 47<br>
Survived: 30<br>
Passengers from Queenstown also showed a better survival ratio compared to Southampton passengers.

#### Conclusion

Passengers who embarked from C and Q had better survival rates compared to passengers from S. Southampton had the highest number of passengers and also the highest number of deaths.

## Feature Encoding
Before performing feature selection and multivariate analysis, I converted the categorical features into numerical format using One Hot Encoding.<br>
Machine learning algorithms and correlation analysis require numerical input, so categorical columns such as Sex and Embarked were encoded into numerical values.

#### Why One Hot Encoding?
Machine learning models cannot directly process categorical data.<br>
Correlation matrices only work with numerical features.<br>
One Hot Encoding helps represent categorical values without introducing ordinal relationships.
Features Encoded<br>
The following categorical columns were encoded:<br>
Sex
Embarked

## Correlation Matrix Analysis
After converting categorical features into numerical format, I used a correlation matrix to understand the relationships between features and identify which variables are most related to survival.

#### Observations
Fare shows a moderate positive correlation with Survived (0.26).<br>
This indicates that passengers who paid higher fares had better chances of survival.<br>
Pclass shows a moderate negative correlation with Survived (-0.34).<br>
Lower class numbers represent higher passenger classes, so first-class passengers had higher survival rates.<br>
SibSp and Parch have a positive correlation (0.41) with each other.<br>
This indicates that passengers traveling with siblings/spouses were also likely traveling with parents/children.<br>
Age has a weak negative correlation with survival (-0.068), showing that age had only a small effect on survival.
sex has strong negative correlation with survival(-0.54), showing that<br>
As the value for Sex_male increases (male passengers), the survival rate decreases.<br>
This indicates that male passengers were less likely to survive.<br>
Female passengers had a much higher chance of survival compared to males.<br>


## Finally
#### Key Insights<br>
Most passengers belonged to third class.<br>
Female passengers had a much higher survival rate than male passengers.<br>
First-class passengers had better chances of survival.<br>
Higher ticket fares were associated with higher survival rates.<br>
Most passengers traveling alone had lower survival chances.<br>
Small families had better survival rates compared to very large families.<br>
Sex, Pclass, and Fare were the most important features related to survival.<br>
