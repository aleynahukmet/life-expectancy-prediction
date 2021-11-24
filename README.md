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
