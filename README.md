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
- [Insights of Data & Conclusion](#insights-of-data--conclusion)
- [Closing Remarks](#closing-remarks)
- [References](#references)


# About

This is Team 1's mini-project for SC1015 (Introduction to Data Science and Artificial Intelligence) with a primary focus on the crime rates and crime types in the state of Washington DC.  

# Team 1 Members 
| Name              |                     Area of Focus                     |GitHub Acount|
|---|:---:|---|
| Saniya Rohit Jamwal |      GitHub Repository, Video Presentation, EDA,         |@saniyajamwal|
| Jarel Tan     |       Dataset, Problem Definition, EDA      |-|
| Chi Seo Hyeon |        EDA        |-|

## Question/Problem Definition 
Crime occurs in every country and yet it is something no country has found a solution to. This got us thinking on the correlation between the crime rates and motivations for committing such heinous acts while specifically looking at avaricious crimes. This brought us to our question:

>*How does household income and home value affect crime types and crime rates?*

# Dataset Selection & Preparation
After extensive online research, our team finalised on a dataset we found to be suitable for our project. We decided to take the crime rate statistics from the United States of America and specifically the state of Wahington DC as this allowed us to work with a larger data set from [OpenDataDC](https://opendata.dc.gov/search?collection=Dataset).

However, the data sets on OpenDataDC are quite extensive and seperated so our team had to complie all the necessary data into [dc_crime_add_vars.csv.zip](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/51e73c4a0e0b5e13d154730405f55643c7f60f4e/dc_crime_add_vars.csv.zip). Furthermore, we honed in further on the data so as to make our problem definition more focused and this was done by analyizing the data from [CRIME_EXTRA.csv](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/51e73c4a0e0b5e13d154730405f55643c7f60f4e/CRIME_EXTRA.csv).

# Exploratory Data Analysis
For our Exploratory Data Analysis we collaborated in a jupyter notebook titled [Final EDA.ipynb](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/51e73c4a0e0b5e13d154730405f55643c7f60f4e/Final%20EDA.ipynb) and these are our findings:

## Income Distribution 
When looking at the data, the offensors were categorised by race and income and we decided to choose the later as the cause of motivation for commiting the crime. This hence made income distribution the focus for our project. 

<ins>Median and mean income for each ward</ins>
| Ward | Median Household Income | Mean Household Income |
|:---:|:---:|:---:|
| 1 |          80,794         |        103,071        |
| 2 |          99,422         |        139,194        |
| 3 |         109,909         |        169,377        |
| 4 |          71,545         |        107,147        |
| 5 |          55,063         |        72,859         |
| 6 |          90,903         |        112,711        |
| 7 |          39,828         |        52,721         |
| 8 |          31,642         |        43,423         |

## Property Values

Having access to a data set comprising of home values, our team decided that it would be worth to take a look at that as well since income and home value are correlated. Higher income means residents are better able to afford higher value homes.

<ins>Median home value for each ward</ins>
| Ward | Median Home Value |
|:---:|:---:|
| 1 |          511,500         |
| 2 |          605,700|
| 3 |         788,800         |
| 4 |          470,500         |
| 5 |          358,200         |
| 6 |          541,100         |
| 7 |          230,700         |
| 8 |         232,100        |

