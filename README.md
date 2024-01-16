# Sentiment Analysis of Amazon Product Review
## Problem Statement
Amazon provides a platform for small businesses and resource-limited companies to expand their reach. Due to its widespread popularity, individuals invest time in crafting detailed reviews, offering insights into both the brand and the product. Analyzing this substantial data pool can provide valuable information to companies, guiding them on product improvement strategies. However, the sheer volume of data surpasses human capacity for analysis.
## Objective
 * Develop traditional supervised machine learning model and deep learning model for sentiment analysis of Amazon product reviews 
 * Compare the models' performance

## Data Collection
The dataset is collected from the official website of the Department of Computer Science and Engineering (CSE) at the University of California, San Diego (UCSD) <br>
Website url: https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/

## Data Description
The data set contains the following columns <br>
* overall : Rating columns that have 1-5
* verified : Has "True" or "False" boolean data to check whether the review is verified or not
* reviewTime : Date
* reviewerID : ID of the customer
* asin : Amazon Standard Identification Number
* reviewerName : Name of the reviewer
* reviewText : Review
* summary : Summary of review
* unixReviewTime: Timestamp in Unix time format
* vote :
* style : Related to image
* image : Image
I droped all the unnecessary columns. Kept  overall, reviewTime, reviewText, summary

## Workflow
Step-1: Pre-Processing
   * Import Dataset
   * Deleted the unnecessary data
   * Export data in parquet formate
<br>Step-2:  EDA - Exploratory Data Analysis
