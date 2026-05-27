# Google-Data-Analytics-Capstone-Bellabeat-Case-Study

This case study is a part of the Google Data Analytics Professional Certificate through Coursera.

This Article will show how I approached and completed the Case Study where I will be acting as a junior Data Analyst for Bellabeat, where I will be analysing customer data to help them guide their marketing team.

## Quick Links 

## Table of Contents 

## Introduction

### Scenario
I am assuming to be a junior data analyst working with the marketing team at Bellabeat, a manufacturer of health-focused products for women. I have been tasked with analysing customers using non-Bellabeat smart devices and pick one product to apply these insights to help with the marketing strategy. The Chief Creative Officer believes that analyzing smart device fitness data could help unlock new growth opportunities for the company.Therefore, Bellabeats executives must approve our recommendations so they must be backed up with compelling data insights and professional data visualizations.

#### Bellabeat Overview
Bellabeat is a high-tech company that manufactures health-focused smart products that informs and inspires women around the world. It collects data on activity, sleep, stress, and reproductive health that empowers women with knowledge about their own health and habits.

#### Company History 
Founded in 2013 by Urška Sršen and Sando Mur, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women.By 2016,Bellabeat had opened offices around the world and launched multiple products.

#### Marketing Strategy
The company has invested in traditional advertising media, such as radio, out-of-home billboards, print, and television, but focuses on digital marketing extensively. Bellabeat invests year-round in Google Search, maintaining active Facebook and Instagram pages, and consistently engages consumers on Twitter. Additionally, Bellabeat runs video ads on Youtube and display ads on the Google Display Network to support campaigns around key marketing dates

#### Objective 
Sršen knows that an analysis of Bellabeat’s available consumer data would reveal moreopportunities for growth. She has asked the marketing analytics team to focus on a Bellabeat product and analyze smart device usage data in order to gain insight into how people are already using their smart devices. Then, using this information, she would like high-level recommendations for how these trends can inform Bellabeat marketing strategy.

## Data Analysis Process
This case study follows the 6 steps of the Data Analysis process: ASK, PREPARE, PROCESS, ANALYZE, SHARE, and ACT. Excel, R and RStudio are utilized for data analysis due to the large dataset size.

## 1. ASK 
### Objective 
Identify ways in which users use non-Bellabeat smart devices and then select 1 product to apply the insights into the final presenation

### Analysis Questions 
The goal of this analysis is to identify trends in how consumers use non-Bellabeat smart devices. These insights will be applied to [Insert Chosen Product Name] to provide high-level recommendations for Bellabeat's marketing strategy, ultimately helping the company unlock new growth opportunities.

### Key Stakeholders
1. Urška Sršen and Sando Mur:
2. Bellabeat marketing analytics team
3. Bellabeat Executives 


**Data Source**: The data used for this project is the [Fitbit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit?resource=download) dataset that was made available through [Mobius](https://www.kaggle.com/arashnic) via Kaggle.

**Licensing** : [CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/)

**Reliable**: 30 users Fitbit Users have consented to the submission of their personal data to be used and does not contain any personal identifiable information such as their height, profession, gender, etc..

**Comprehensive**: It contains information about the minute-level details and daily output of the user's heart rate, sleep monitoring, physical activity and calories

Note: While the data is from 2016, the behavioral patterns regarding sedentary activity and sleep remain relevant for current market trends.


## 2.Prepare
After downloading data, I was able to extract it and saw that there were 18 csv files in total, but I am choosing to focus on these 6:

dailyActivity_merged.csv


dailyCalories_merged.csv


dailyIntensities_merged.csv


dailySteps_merged.csv


sleepDay_merged.csv


weightLogInfo_merged.csv

For this project, I chose to use Google Sheets as the primary processing tool. While coding languages offer automation, spreadsheet analysis provides rapid iteration, allowing me to manipulate the data and validate the data for cleaning.

It also ensures that the data can be easily understood by non-technical stakeholders, bridging the gap between raw backend data and final executive reporting.


## 3. Process

In this step, I processed the data to keep the formats consistent across the files.


### Data Cleaning & Transformation Steps

**Data Normalization**: I aligned inconsistent Date/Time formats across datasets by separating the timestamps and applying standardized date formatting to ensure valid data merging.

**Data Integrity Audit**: I conducted an audit to identify and handle duplicate records and missing values. Where missing data was identified, I used IFERROR logic to handle null values as 0, preventing skew in aggregate calculations.

**Relational Merging**: I established a unique "Helper Key", which is a combination of Id + Date, to perform VLOOKUP operations. This allowed me to merge user activity metrics with sleep logs, enabling cross-functional analysis.

**Verification**: After every manipulation, I performed a "spot-check" validation against the original raw files to ensure 100% data fidelity.


## 4. Analyze

Now that the data has been cleaned and normalised, I can look for trends and relationships within the dataset 

### Analysis 1- User Activity levels across the week
From this analysis, I was able to uncover the "Sunday Effect" across the users. This indicates a clear shift in the users's lifestyle routine towards the end of the week 

**Trends** : User Activity is seen to be the lowest on Sunday but it has the maximum sleep duration. This shows that the users use Sundays as a Recovery phase. On the otherhand, Mondays have an increased activity level but less sleep duration.


**Buisness Insight** : This pattern suggests that users may be experiencing stress when starting the work week, that may be resulting in a difficulty maintaining a quality sleep as the work week begins.


**Marketing Reccomendation** : Bellabeat could use this insights to promote a more relaxed approach such as a "Sunday Reset" notifiation to encourage the users to do some light activities such as yoga and an earlier bedtime on Sunday. This could also inlcude mindfullness excercises on Monday Mornings to increase app engagement.

<img width="392" height="270" alt="image" src="https://github.com/user-attachments/assets/6723464a-0486-44ed-b9fc-0738dd316d61" /> 


Fig 1. Pivot table - User Activity 


<img width="392" height="266" alt="image" src="https://github.com/user-attachments/assets/72a9f1f9-1d12-4219-b319-54485543891f" />


Fig 2. Pivot table - Sleep Minutes 









