# Amazon-Music-Reviews <!-- omit in toc -->

Amazon has transformed the way we shop and has set high standards with its same day delivery and customer support services. With the transition to onlinw shopping, we rely heavily on images and customer reviews when making a decision on what to buy. 

#### -- Project Status: [Completed]

# Table of Contents <!-- omit in toc -->

- [Synopsis](#synopsis)
- [Dataset](#dataset)
  - [Summary of the Dataset](#summary-of-the-dataset)
  - [Exploratory Analysis](#eda)
- [Sentiment Analysis and Review Prediction](#sentiment)
  - [Multi-class classifcation](#classification)
  - [Neural Networks - LSTM](#lstm)
- [Conclusion](#conclusion)

# Synopsis <a name="synopsis"></a>

Amazon which was once started as an online book-store is now company with a market cap of over $1.5 Trillion and is posied to grow with its annocuments of entry in the drug distribution and telemedicine industry. The crux of the business however still lies in the online reail businees which has grown at a rapid pace due to the pandemic. 

The purpose of this project is to analyze the review data for products on amazon music and train a sentiment analysis model to predict the user ratings to demonstrate the power of NLP and Neural Networks. 

# Dataset <a name="dataset"></a>

The datasets used for this part of the project can be found on Kaggle: 

https://www.kaggle.com/c/mie1624winter2021/data

## Summary of the Dataset <a name="summary-of-the-dataset"></a>

 - The dataset contains twitter id of user and reviewed products. Textual review, summary and a numerical rating between 1-5. 
 - The price column is however stored as strings and contains text in some cases.
 - The dataset is cleaned by converting the price values to numerical and imputing and missing price value by the median. The textual data from the summary and review is combined and cleaned by removing stop words, punctuations and lemmetizing. 

## Exploratory Analysis <a name="eda"></a>

 - From the plot below, it can be seen that majority of the ratings are 4 or 5. Which contradicts the initial itution that people only go to review something when they find it bad or not up to the mark. This might be a more special case since the data is for musical instruments and usually enthusiasts get something only when they know what they are getting.

  ![Overall Ratings](images/Distribution_of_ratings.png)

- Most reviewed genre was Pop followed by Alternative Rock. 

  ![Genre Ratings](images/Distribution_of_ratings_category.png)

- The following are the most reviewed products and the most active users.

  ![Most Reviewed](images/Top_reviewed.png)
  
  ![Most Active](images/Top_reviewers.png)
  
 - Sentiment distribution of most reviewed products.
 
  ![Most Reviewed Sentiment](images/Top_reviewed_sentiments.png)
 
 
# Sentiment Analysis and Review Prediction <a name="sentiment"></a>


## Conclusion <a name="conclusion"></a>

Supervised learning algorithms can then be trained on pre-clustered data to predict the clusters of new and unseen articles. This is a powerful tool and is currently being used by companies like Google for news clustering.

When training a logsitic regression model on the data and 15 clusters, an accuracy score of 0.97 was obtained for the train data and 0.94 for the test/validation data.

