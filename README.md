# Multiple Indicies Affect on Unemployment Rate

## Obejective of this Analysis
The objective of this analysis is to examine the effect of multiple economic indices on the unemployment rate in the US. The unemployment rate will be the dependent variable for this analysis whereas the following variables will serve as the independent variables; Gross Domestic Product (GDP), Producer Price Index (PPI), Consumer Price Index (CPI), Federal Fund Rate, and the National Interest Rate. The machine leaning technique this analysis will employ will consist of a linear regression to explore the relationship between the selected indices and the dependent variable.   

## Data Sources:
For this analysis, we have 6 different CSV datasets. Each dataset represents a factor that we want to analyze in relation to the Unemployment Rate. This includes CPI, PPI, GDP, Inflation Rate, and the Federal Fund Rate.

## Team Roles and Responsibilities


David Fleming: Presentation

Ariana Colon : Machine Learning Model

Helen Garcia: GitHub

Adrian Maple: Dashboard

Martin Fonseca: Dashboard

## Data
Tools: 
Python, SQL, Supervised Machine Learning, Javascript, Jupyter Notebook, HTML, JavaScript, CSS

We mapped our data, which can is shown in the ERD below:

![ERDNEW](https://user-images.githubusercontent.com/108022219/199629591-831249d7-e8e6-4d46-8c64-de55ae7df61b.png)



We are using PgAdmin SQL to create our database. The database was created with 6 tables from each csv file and joined into a new table called Unemployment_table seen below. We used the code below to join 6 tables by using 5 left joins.

<img width="520" alt="Screen Shot 2022-11-09 at 7 16 20 PM" src="https://user-images.githubusercontent.com/107590196/200969479-204a8aeb-f9e7-4ace-affd-03d9e3a7a0d9.png">


![Screen Shot 2022-11-02 at 7 26 27 PM](https://user-images.githubusercontent.com/107590196/199621018-86c851d5-8eb9-49e1-8078-5c65c73f5bcf.png)



## Selected Topic
The selected topic is to analyze the relationship between Unemployment Rate and Federal Funds Interest Rates. Specifically, we want to predict how Federal Funds Interest Rates change will affect Unemployment Rate.

## Reason of Selected Topic
Unemployment in America has been volatile in the US over the past 20 years. Major events such as the housing market crash of 2009 and the COVID pandemic have affected the employment of many Americans that have lived through these events. The purpose for our analysis is to examine and identify the major economic indicators that may influence the unemployment rate in the US. By understanding these relationships, we hope to better understand how our individual industries that we work in may contribute to the volatility of the unemployement rate year over year.  

## Questions We Want Answered
1. Which indicies had the largest impact on the Unemployment Rate over the past 20 years?
2. What is the measured change of each index over the stated time period? 

## Machine Learning Model Requirements
* Data Preprocessing
    * For MultipleLinearRegression, preliminary data preprocessing begins with making sure our data from our PostgresSQL database table is loaded into a dataframe and is all in numerical values. Because the date column was not initially a numerical value, we formatted its data type into an integer. The next step was to scale the unemployment dataframe from 0 to 1 with the MinMaxScaler module. Once scaled, the features set and target set from the unemployment database are defined. The features set entails the following columns: GDP, PPI, Inflation_Rate, CPI, Interest Rates. The target set is the unemployment_rate column.
* Feature Engineering/Selection & Model Choice Explanation
    * Because our data contains continuous variables from 2001 to 2021, we decided to use Multiple Linear Regression. This feature selection takes in a set of factors and attempts to learn their patterns on a specific value, in this case, unemployment rate.
* How Data was Split
    * The data was split into training and testing sets before it was fit for MultipleLinearRegression with 75% of the data being for training and the other 25% was testing.
* Limitations and Benefits
    * A benefit of Multiple Linear Regression is if new data feature points are added, Linear Regression can be used to predict the result of unemployment rate. A limitation is it might present how there is no relationship with the data if there is no linear slope.
* Model Changes/How Model has been Trained
   * A change we made to the model was plotting scatter plots that include the linear regression equation instead of scatter plots with only data points. This change allows us to highlight the specific relationships each independent variable has on the unemployment rate. A second change we made to the model is graphing the relationship between CDP and CPI because their individual graphs against unemployment rate were similar. Their graph together displayed a linear relationship among these two features. Since we only have numerical data, we decided to try a KMeans machine learning model and see how the 3 PCA components would be clustered together. After this attempt, we decided to stick to Linear Regression mdoel since the main questions we want answered require a machine learning model for continuous data. 
* Regression Score
   * The model produced a R2 value of 0.6828, indicating our model explains about 68% of the variation between the variables.
## Link to Google Slides

https://docs.google.com/presentation/d/1lzQ-b4w2ID-vXFYUGq4Te_y_GC6d6SaXZiabudDA7Ns/edit?usp=sharing

## Link to Dashboards

https://admaple.github.io/
