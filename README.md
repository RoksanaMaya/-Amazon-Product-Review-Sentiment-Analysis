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

## Workflow for Machine Learning Algorithms
* **Step-1: Pre-Processing**
   * Import Dataset
   * Deleted the unnecessary data
   * Export data in parquet formate
     <br>
* **Step-2:  EDA - Exploratory Data Analysis**
  * Checked structural information
  * Checked and handled missing values
  * Checked and handled outliers
  * Visualize the columns using different charts like count plot, whisker plot, and others
  * Filtered out the necessary columns
* **Step-3:  NLP - Natural Language Processing**
  * Convert text to lowercase
  * Remove punctuations, non-character, emojis
  * Tokenization
  * Lemmatization
  * Stop word removal
  * Wordcloud Analysis
* **Step-4:  Feature Engineering**
  * TF-IDF : Text Frequency- Inverse Document Frequency
  * Dimensionality reduction: PCA
* **Step-5:  Model Creation**
  * RandomizedSearchCV
  * Fit the following models for classification
    * Naive Bayes
    * Random Forest Classifier
    * Support Vector Machine
    * Logistic Regression
    * GBoosting: Gradient Boosting
    * XGBoosting- Extreme Gradient Boosting
* **Step-6:  Model Performance Evaluation**
* **Step-7: Performance Evaluation**
  
  | model | accuracy_score | f1_score | precision_score | recall_score |
  |----------|----------|----------|
  | Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3 |Row 1, Col 2 | Row 1, Col 3 |
  | Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3 |Row 1, Col 2 | Row 1, Col 3 |
  | Row 3, Col 1 | Row 3, Col 2 | Row 3, Col 3 |Row 1, Col 2 | Row 1, Col 3 |
## Workflow for Deep Learning Algorithm
* **Step-1: Pre-Processing**
   * Import Dataset
   * Deleted the unnecessary data
   * Export data in parquet formate
     <br>
* **Step-2:  EDA - Exploratory Data Analysis**
  * Checked structural information
  * Checked and handled missing values
  * Checked and handled outliers
  * Visualize the columns using different charts like count plot, whisker plot, and others
  * Filtered out the necessary columns
* **Step-3:  NLP - Natural Language Processing**
  * Label encoding: one_hot_key
  * Tokenization
  * Creating Sequence
  * Padding
* **Step-4:  Model Creation**
  * LSTM
* **Step-6:  Model Performance Evaluation**
