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
    - [Crime rates](#crime-rates)
    - [General Trend](#general-trend)
    - [Interesting Outlier](#interesting-outlier)
- [Techniques](#techniques)
    - [GeoPandas and Heat Maps](#geopandas-and-heat-maps)
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

Our goal in choosing this topic for study was to identify and determine the significance of certain factors in the frequency of crime occurrences.

# Dataset Selection & Preparation
After extensive online research, our team finalised on a dataset we found to be suitable for our project. We decided to take the crime rate statistics from the United States of America and specifically the state of Wahington DC as this allowed us to work with a larger data set from [OpenDataDC](https://opendata.dc.gov/search?collection=Dataset).

However, the data sets on OpenDataDC are quite extensive and seperated so our team had to complie all the necessary data into [dc_crime_add_vars.csv.zip](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/51e73c4a0e0b5e13d154730405f55643c7f60f4e/dc_crime_add_vars.csv.zip). From the dataset that we have obtained, we can notice that the most common categorization of crimes are theft, robbery and assault. Furthermore, we honed in further on the data so as to make our problem definition more focused and this was done by analyizing the data from [CRIME_EXTRA.csv](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/51e73c4a0e0b5e13d154730405f55643c7f60f4e/CRIME_EXTRA.csv).

# Exploratory Data Analysis
To prepare our data for analysis, we first obtained the necessary data sets online and initialized the jupyter notebook with relevant imports. We then merged the two data sets, and extracted, or filtered out, the data that we have selected for analysis. For our Exploratory Data Analysis we collaborated in a jupyter notebook titled [Final EDA.ipynb](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/51e73c4a0e0b5e13d154730405f55643c7f60f4e/Final%20EDA.ipynb) and these are our findings:

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

## Crime rates 
From our prepared data, we printed visual representation to better understand the data distribution and help identify a pattern, trend or anomaly. Histograms were helpful in displaying the distribution of crime occurrences

![image](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/d87030fef4bf22da81769207bff1ad1ddbfc995c/crime%20rates%20by%20wards_histogram.png)

## General trend
With the help of these graphic aid, certain observations could be made; a trend could be identified from how the wards with lower income have lower crime rates relative to other wards with higher income; as a majority of crimes listed in the dataset are theft, robbery and other property-related crime , the most probable explanation would be that there is more to gain in higher-income wards.
<ins>Median income by ward</ins>
| Ward | Median Household Income |
|:---:|:---:|
| 1 |          80,794         |
| 2 |          99,422         |
| 3 |         109,909         |
| 4 |          71,545         |
| 5 |          55,063         |
| 6 |          90,903         |
| 7 |          39,828         |
| 8 |          31,642         |

## Interesting Outlier
However, an anomaly can also be spotted in our observation; ward 3, with the highest income and home value, has an extremely low frequency of crime occurrence compared to other wards. A possible argument for how this is possible would be that the high income and home value is a direct reflection of high security, high safety systems to prevent such crimes, although this argument is weak as ward 2 stands right behind ward 3 in terms of income but runs first for the highest crime rate among all the wards.

# Techniques 

## GeoPandas and Heat Maps 
Among the several techniques used in the project to aid with data analysis and interpretation is the use of the geopanda module and heatmaps. The geopanda module is an extension of the pandas module, which allows for spatial operations on geometric types; this gives room for a more thorough manipulation of data, for easier interpretation and visual representation of our dataset.

Heatmaps were also utilized as a method of displaying data; as observable from the previous data exploration slides, the data that we have used can be effectively represented with a heatmap. Since visual aid is one of the most important methods of communicating data, we felt that this was a point worth mentioning.

![image](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/df208f7ecf1c54d318dfde8e4a2f10a879f14429/median%20income%20distribution%20by%20ward.png)
![image](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/df208f7ecf1c54d318dfde8e4a2f10a879f14429/median%20home%20value%20distribtuion%20by%20ward.png)

# Insights of Data & Conclusion

We then decided to investigate further into several other factors; such as the crime type in different wards. To no surprise, violent crimes, such as assault, attempted murder and murder, were more often committed in lower income wards compared to higher income wards.

![image](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/6ffa9a93e62f01d7e9ed6a08e1ac53111ecbcbd6/crime%20types%20by%20ward.png)

This is most likely a result of the high-security, high-safety systems we mentioned much earlier when describing the abnormally low crime rate in ward 3; because there is more capital to invest into security systems, whether it be automated machinery or hired labor, to prevent crimes, especially violent crimes, from occurring. These methods of prevention may not seem to have functioned optimally, as we can observe that overall crime rate tends to be higher in high income wards.

![image](https://github.com/saniyajamwal/sc1015-Group-Proj/blob/c41961d1f221bef7d86c01dc8a92abe68d18b88b/types%20of%20crime.png)

But this means that the percentage of violent crimes are much higher in lower income wards; probably due to the fact that the criminals in lower income wards are aware of the absence of security, causing them to be more daring and aggressive compared to criminals that attempt to commit a crime in higher income wards, where it is crucial to not create a ruckus to avoid getting caught. This observation may not seem that important, but it does pretty well in outlining the effects of income discrepancy in society; how varying economic stability affect safety and order of a community, and how economic instability can cause unwanted violence and crime.

# Closing Remarks

Through this project, we learnt the importance of relevance in data science; no matter how much data and information are accessible to us, they are just random pieces of information until and unless we transform them into relevant and contextual data through interpreting their significance and identifying the needs to organize them. And through practicing what we have learnt, we were able to identify the significance of income level and wealth distribution in determining the frequency of crime; polarization and income discrepancy is indeed a very impactful factor, and is one of the main driving cause of crime occurrences, at least from our observations in this mini project. 

Apprehended criminals were often found to be from an unstable economic background, with crimes happening most frequently in higher-income regions where there’s more to gain; the fact that we can categorize regions by income levels is by itself a testament to the perpetually existing social problem of polarization. This problem is not something that can be fixed immediately; it’s a terminal symptom of capitalism, and can only be alleviated, not completely removed. And the first and most important step of alleviating this said problem is to identify it. Through filtering, interpreting, organizing and analyzing, we have already identified the problem; what is left is to spread awareness and spark action.

This project was a product of hard work and research and I would like to thank my groupmates for their efforts and collaboration. The past few weeks have been a journey, learning many new concepts and ideas.

# References

-[Camera-enforcement-locations](https://opendata.dc.gov/datasets/camera-enforcement-locations)
-[Traffic-camera](https://opendata.dc.gov/datasets/traffic-camera)
-[GIS](https://www.arcgis.com/home/webmap/viewer.html?webmap=c88bff76cd3e4568800a19e9f361822e)
-[Crime-incidents-in-2017](https://opendata.dc.gov/datasets/crime-incidents-in-2017/data)
-[Crime-incidents-in-2016](https://opendata.dc.gov/datasets/crime-incidents-in-2016)
-[Crime-incidents-in-2015](https://opendata.dc.gov/datasets/crime-incidents-in-2015)
-[Crime-incidents-in-2014](https://opendata.dc.gov/datasets/crime-incidents-in-2014)
-[Crime-incidents-in-2013](https://opendata.dc.gov/datasets/crime-incidents-in-2013)
-[Crime-incidents-in-2012](https://opendata.dc.gov/datasets/crime-incidents-in-2012)
-[Real-property-tax-assessment-neighborhoods](http://opendata.dc.gov/datasets/real-property-tax-assessment-neighborhoods) 
-[Real-property-tax-assessment-sub-neighborhoods](http://opendata.dc.gov/datasets/real-property-tax-assessment-sub-neighborhoods)
-[house-prices-us#data](https://datahub.io/core/house-prices-us#data)



