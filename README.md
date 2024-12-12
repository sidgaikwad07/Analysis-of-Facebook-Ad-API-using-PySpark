# Big Data Analysis of Facebook Ad Library API Dataset Using PySpark
This is a repository implementing and analyzing the Facebook Ad Library API Dataset by using Big Data Analytics, PySpark. It covers key political advertising trends in Australia from March 2020 to February 2024, including the 2022 Federal Election and the 2023 Voice Referendum.

## Table of Contents
1. Introduction
2. Objectives
3. Dataset Overview
4. Pre-processing Steps
5. Analysis & key Findings
6. Technologies & Libraries Used
7. Setup Instructions
8. Results
9. Future Work

## 1. Introduction
This project shows how Big Data Analytics can extract insight from big datasets. PySpark and distributed computing are used in this analysis, focusing on:
### i) Ad volume trends.
### ii) Demographic targeting
### iii) Political spending during elections and referendums.
This effort showcases the strengths of using distributed systems to handle very large datasets with scalability, speed, and fault-tolerant features.

## 2. Objectives
The below mentioned are the objectives of the project : 
### i) Analyze political advertising trends in Australia from 2020 to 2024.
### ii) Analyze ad spend across demographics and regions.
### iii) Research targeting strategies of political parties and advocacy groups.
### iv) Use PySpark to process huge volumes of data.

## 3. Dataset Overview
The below is the Overview of the Dataset :
### i) Source: Facebook Ad Library API.
### ii) Scope: Australian users from March 2020 to February 2024.
### iii) Description : This dataset contains sponsored political posts on Facebook that target Australian users, and includes the period prior to:
    1) The Australian Federal Election in May 2022.
    2) The Voice Referendum in October 2023.
### iv) Size: 39.53 million records in JSON format.
### v) Key Attributes: ad_creation_time
      1) ad_creative_body
      2) impressions
      3) demographic_distribution
      4) region_distribution
### vi) Challenges: High data volume, variety, and complexity.

## 4. Pre-processing Steps
### i) Data Cleaning: Replaced null values with empty strings.
### ii) Deduplication: Removed duplicate records to reduce data dimensions.
### iii) Data Filtering : Focused on specific topics and political alignments.
### iv) Feature Engineering:
      1) Extracted Year, Month, and Day from ad_creation_time.
      2) Converted Nested JSON fields into structured format.

## 5. Analysis & Key Findings
## Key Insights
### i) Political Advertising:
      1) Major Parties like Labour, Liberal, and Greens dominate ad spending.
      2) Government departments also use Facebook ads for public awareness.
### ii) Trending Topics:
      1) Hastags like #auspol, #climateaction, and #MorrisonMustGo reflect political and social discourse.
### iii) Demographic Insights:
      1) Male audiences receive more ad spend compared to females.
### iv) Regional Focus:
      1) Ads are concentrated in populous regions like Victoria, NSW, and Queensland.
      2) Some international reach observed in places like Bali and New York.
### v) Visualization Highlights
      1) Word Clouds: Highlighted frequent terms in political and advocacy ads.
      2) Bar Charts: Showcased top funding entities and regions by ad volume.
      3) Line Plots: Tracked ad spend trends over time.

## 6. Technologies & Libraries Used
    1) Big Data Framework: Apache Spark(PySpark)
    2) Data Visualization: Matplotlib, Seaborn, WordCloud
    3) Languages: PySpark
    4) Tools: HDFS for Scalable storage, Distributed computing on DATA7201 cluster.

## 7. Setup Instructions
## Prerequisites

### i) Install Pyspark
    1) pip install pyspark
### ii) Install required libraries
    1) pip install wordcloud nltk matplotlib seaborn
### iii) Download the dataset and place it in the appropriate directory.
### iv) Running the Project
    1) Launch Pyspark and load the dataset:
        from pyspark.sql import SparkSession
        spark = SparkSession.builder.appName("FacebookAdAnalysis").getOrCreate()
        data = spark.read.format("json").load("<path_to_dataset>")
    2) Perform preprocessing, analysis, and visualization using the provided scripts.

## 8. Results
### i) Ad Spend Trends: Notable spikes during the 2022 Federal Election and the 2023 voice referendem.
### ii) Demographics: Males are the primary target audience for political ads.
### iii) Regional Distribution: Ads were concentrated in urban areas but included some international outreach.

## 9. Future Works
### i) Integrate granular demographic data for detailed insights into age, gender, and regional ad targeting.
### ii) Analyze temporal trends with finer resolution to capture event-specific patterns.
### iii) Construct predictive machine learning models for the forecast of campaign impact.




