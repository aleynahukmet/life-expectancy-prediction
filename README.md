# life-expectancy-prediction
<p align="center"> 
   <img width="1000" height="400" alt="Ekran Resmi 2021-06-28 01 15 28" src="https://user-images.githubusercontent.com/52889449/143092733-90e1665f-5de4-4eae-9fe6-6b7f4c462e2c.jpg">
</p>

This project aims to predict the life expectancy of people depending on some other features. While predicting life expectancy on people whose in different circumstances using machine learning models on data helps us better understand the effect of features on life expectancy and determine how they change it.

# Dataset

The Global Health Observatory (GHO) data repository under World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries. The data sets are made available to the public for health data analysis. The data-set related to life expectancy, health factors for 193 countries have been collected from the same WHO data repository website. Among all categories of health-related factors, only those critical factors were chosen which are more representative. It has been observed that in the past 15 years, there has been a huge development in the health sector resulting in improvement of human mortality rates especially in the developing nations in comparison to the past 30 years. Therefore, in this project, we have considered data from the year 2000-2015 for 193 countries for further analysis.

# Data Preprocessing

First of all, I changed the column names to lower case to make it a clear dataset and filled the spaces between them. Then I checked for duplicated rows and saw there was none. While filling the missing values, according to dataset containing many outliers and also skewed distribution, I used the median method.

# Exploratory Data Analysis

I used some visualization methods to have a better understanding of features' relation, and also their effects on life expectancy.Initially, I plotted the count of numerical variables among the dataset with histplot. I only had two categorical features, country and status. Status was showing whether a country was developing or developed. I plotted the count of status distribution with catplot.

<p align="center"> 
   <img alt="Ekran Resmi 2021-06-28 01 15 28" src="https://user-images.githubusercontent.com/87663976/143217634-99cb184b-1684-4c50-b22c-88733deeb62e.png">
</p>
Then I wanted to show the relation between life expectancy and other features. I first visualized the top ten countries with the highest life expectancy with a barplot. After that, I plotted a scatter plot of life expectancy with other features, it did not only make a better understanding of the relation between features and life expectancy but also showed there were outliers in our dataset. To see outliers better I plotted a boxplot to visualize them. Many variables on our dataset including the target variable (life expectancy) had outliers. But I let the outliers stay and decided to deal with them later.

# Correlation 

<p align="center"> 
   <img alt="Ekran Resmi 2021-06-28 01 15 28" src="https://user-images.githubusercontent.com/87663976/143219223-4451b45d-d5ab-4aaa-86a4-37caf145171a.png">
</p>

As it can be seen on the correlation matrix some features had a high correlation between them. When independent features are highly correlated i.e. have the same nature, then they introduce the element of variance in the model which is called Multi-Collinearity. Multi-Collinearity is not good for our models so I dropped some of the columns to avoid that.

# Label Encoding
We had only two categorical columns. When it comes to the "status" column, the ordinal column is encoded with the label encoding method. The "country" column is nominal and it is encoded with the one-hot encoding method. And I encoded "country" column with one-hot encoding method I dropped one column to avoid Multi-Collinearity.

# Feature Scaling
Robust Scaler is one of the best scaler methods to use when a dataset contains outliers. As seen previously, our dataset had outliers and we did not remove or replace them. Outliers can skew a probability distribution and make data scaling using standardization difficult as the calculated mean and standard deviation will be skewed by the presence of the outliers. Therefore, we choose RobustScaler for our Feature scaling.

# Models 
We trained eight different models (Lasso, Ridge, Random Forest, KNN, Decision Tree, SVR, Gradient Boosting Regressor and Ada Boosting Regregssor) to see which one is the giving best results. Then I checked results after cross validation too and plotted the results.
<p align="center"> 
   <img alt="Ekran Resmi 2021-06-28 01 15 28" src="https://user-images.githubusercontent.com/87663976/143229476-dfa19181-73d5-4a0b-8919-763ec6d82cc6.png">
</p>
