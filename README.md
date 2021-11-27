# House-Price-Prediction
Advanced Regression - Ridge and Lasso Regression

A US-based housing company has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. 
The company is looking at prospective properties to buy to enter the market.

The problem was APPROACHED in the following manner:-

1. What the Company wants:
	The company wants to know the following things about the prospective properties:
* Which variables are significant in predicting the price of a house, and
* How well those variables describe the price of a house.

2. Business Goal
Wu are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

3. Understanding the Data:
* Data revolves around the SalesPrice, This is the Price of the house. There are many predictor variables like Area, year Sold, sale type, sale condition, data about pools, data about garages, data about veneers etc.
* There are many columns with the high null percentage like pool, fencing, alley etc. These values are not missing at random. The houses without these features will be having null values.
* Similar is the case of variables with less number of missing values. The data is not missing at random.  

4. Data Cleaning
* Dropping the variables with very high null values. Imputing with null or any other variable will make the variable highly skewed.
* Filling “NA” in other categorical variables with missing values.
* Filling “0” in numeric variables.
* Also creating new category for some categorical variable.

5. Exploratory Data Analysis:
a. Univariate Analysis:
i. Histogram and Box plots for numeri variables to check the skewness as well as detecting outliers.
ii. Countplots and pie charts for categorical variables.
iii. Dropping the categorical variables in which one features completely dominates over other.
b. Bivariate Analysis
i. Looking at the numeric variables against the target variable and looking at features, which are showing some relation with Sales Price of the house.
ii. Pair plots and Heat map to detect relation between various features.
iii. Box plots for categorical variable against the target variable.

6. Feature Engineering
It is the most important part of the project. In this we have built many features like:
a. Has_veneer
b. Has_basement
c. Has_fireplace
d. Has_Garage
These features can play good role in determining the price of the house.

7. Data Preparation for Modelling:
a. Handling the skewness in Target variable and other numeric variables using power-transformer(yeo-johnson)
b. Handling outliers by capping the variable.
c. Dropping the variable regarding the dates like yr_built, yr_sold etc.
d. Ordinal Encoder and dummy encoding for categorical variables.
e. Standardizing the other numeric variables.

8. Model Building 
a. Starting with a Linear Regression model as a proof of concept. Overfitting was observed in case of Linear Regression Model.
b. Based on above, to tackle overfitting Ridge and Lasso Model as built. 
c. Fine tuning the models using Grid search CV technique. 
d. Building several models. Also doubling the value of alpha parameter to check the effect on model.
e. Although, Ridge was giving the best results in terms of R2_score and RMSE value. Lasso Regression model was selected as the final model as it also eliminated some less important features making the model lean.
f. Also the effect of removing the top 5 features in model was checked. Removing the top 5 variables decreased the model’s performance by small amount. But the number of features selected in final model was increased from 54 to 60 when top variables were removed, signifying the importance of top 5 variables. 
