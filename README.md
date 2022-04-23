# SC1015 Mini Project 
Team 1: Jarel Tan, Saniya Jamwal, Chi Seo Hyeon 
## Table of contents
- [About](#about)
- [Team 1 Members](#team-1-members)
- [Question/Problem Definition](#questionproblem-definition)
- [Dataset Selection & Preparation](#dataset-selection--preparation)
    - [OpenDataDC](https://opendata.dc.gov/search?collection=Dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
    - [project final.ipynb](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/main/project%20final.ipynb)
    - [Income Distribution](#income-distribution)
    - [Property Values](#property-values)
    - [General Trend](#general-trend)
    - [Interesting Outlier](#interesting-outlier)
- [Machine Learning](#machine-learning)
    - [ARIMA.ipynb](https://github.com/BLTech-py/sc1015/blob/main/ARIMA.ipynb)
    - [ARIMA Introduction](#arima-introduction)
    - [Best Blk for ML](#best-blk-for-ml)
    - [p, d, q value Optimisation](#p-d-q-value-optimisation)
    - [Obtaining Test Data](#obtaining-test-data)
    - [Future Price Prediction](#future-price-prediction)
- [Insights of Data & Conclusion](#insights-of-data--conclusion)
- [Closing Remarks](#closing-remarks)
- [Version History](#version-history)
- [Extras](#extras)
- [References](#references)


# About

This is Team 1's mini-project for SC1015 (Introduction to Data Science and Artificial Intelligence) with a primary focus on the crime rates in the state of Washington DC.  

# Team 1 Members 
| Name              |                     Area of Focus                     |GitHub Acount|
|---|:---:|---|
| Saniya Rohit Jamwal |        Dataset, GitHub Repository, EDA        |@saniyajamwal|
| Jarel Tan     |     Video Presentation, Machine Learning, EDA      |-|
| Chi Seo Hyeon |       Problem Definition, EDA        |-|

## Question/Problem Definition 
Crime occurs in every country and poverty is something no country is exempt from. This got us thinking on the correlation between the two and how one impacts the other while specifically looking at property-motivated crimes. This brought us to our question:

>*How does household income and home value affect crime types and crime rates?*

# Dataset Selection & Preparation
After extensive online research, our team finalised on a dataset we found to be suitable for our project. We decided to take the crime rate statistics from the United States of America and specifically the state of Wahington DC as this allowed us to work with a larger data set from [OpenDataDC](https://opendata.dc.gov/search?collection=Dataset).

However, the data sets on OpenDataDC are quite extensive and seperated so our team had to complie all the necessary data into [dc_crime_add_vars.csv.zip](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/main/dc_crime_add_vars.csv.zip). Furthermore, we honed in further on the data so as to make our problem definition more focused and this was done by analyizing the data from [CRIME_EXTRA.csv](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/main/CRIME_EXTRA.csv).

# Exploratory Data Analysis
For our Exploratory Data Analysis we collaborated in a jupyter notebook titled [project final.ipynb](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/main/project%20final.ipynb) and these are our findings:

## Income Distribution 
When looking at the data, the offensors were categorised by race and income and we decided to choose the later as the cause of motivation for commiting the crime. This hence made income distribution the focus for our project. 

<ins>Meadian and mean income for each ward</ins>
| Ward | Median Household Income | Mean Household Income |
|---|:---:|---|
|   1  |          80,794         |        103,071        |
|   2  |          99,422         |        139,194        |
|   3  |         109,909         |        169,377        |
|   4  |          71,545         |        107,147        |
|   5  |          55,063         |        72,859         |
|   6  |          90,903         |        112,711        |
|   7  |          39,828         |        52,721         |
|   8  |          31,642         |        43,423         |
