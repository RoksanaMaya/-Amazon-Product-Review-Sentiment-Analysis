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
  |----------|----------|----------|----------|----------|
  |	GNB	| 0.75260 |	0.772652 | 0.714723 |	0.8408 |
  | RF	| 0.77295 |	0.779595 | 0.757427 |	0.8031 |
  | LR	| 0.81765 | 0.824891 | 0.793387 | 0.8590 |
  |	SVM	| 0.81610	| 0.826526 | 0.782182 |	0.8762 |
  |	GB	| 0.83610	| 0.840626 | 0.818036 |	0.8645 |
  | XGB	| 0.82940	| 0.834994 | 0.808485 | 0.8633 |
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
* **Step-6:  Model Performance Evaluation** <br>
  * LSTM performance summary
   ![LSTM performance summary](https://github.com/RoksanaMaya/-Amazon-Product-Review-Sentiment-Analysis/blob/main/Screenshot_2.jpg)

## Challenges
Encountered several challenges during the project including:-
 * Managing the vast and diverse volume of Amazon reviews
 * intricate text preprocessing
 * addressing class imbalance
 * fine-tuning hyperparameters
 * ensuring model interpretability
 * running the model for the huge dataset in the IDE
To overcome these challenges I required careful consideration of computational resources, attention to detail in preprocessing, and strategic optimization of model architectures. Despite these obstacles, the project succeeded in providing valuable insights into sentiment analysis of Amazon product reviews.
## Conclusion

In addressing the challenge of comprehensively analyzing the vast Amazon product review dataset, our objective was to develop and compare traditional supervised machine learning models and a deep learning model for sentiment analysis. The results demonstrated that XGBoosting, among traditional machine learning algorithms, exhibited the highest performance, while LSTM stood out as the superior performer in the realm of deep learning. This dual-pronged approach not only empowers small businesses with actionable insights for product enhancement based on customer sentiments but also highlights the effectiveness of both machine learning paradigms in managing the overwhelming volume of data on the Amazon platform.
## Future Scope
Future enhancements for the sentiment analysis of Amazon product reviews include exploring advanced deep learning architectures like BERT and GPT, implementing transfer learning, incorporating multimodal analysis with images or videos, developing dynamic sentiment analysis models, providing user-specific recommendations, focusing on aspect-based sentiment analysis, establishing real-time monitoring systems, extending capabilities to cross-domain sentiment analysis, improving model explainability, and integrating sentiment analysis insights into customer support systems. These avenues aim to refine sentiment analysis models and offer a more nuanced understanding of customer sentiments in the e-commerce domain.
