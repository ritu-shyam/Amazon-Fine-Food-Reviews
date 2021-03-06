# Amazon-Fine-Food-Reviews
This repository contains a series of experiments performed on the Amazon Reviews dataset.This includes data visualization techniques,NLP related tasks,and prediction by various machine learning models.

The dataset can be downloaded from : https://www.kaggle.com/snap/amazon-fine-food-reviews

## Basic information about the downloaded dataset

  * Number of reviews: 568,454
  * Number of users: 256,059
  * Number of products: 74,258
  * Timespan: Oct 1999 - Oct 2012
  * Number of Attributes/Columns in data: 10
  
## Attribute Information:

  1. Id
  2. ProductId - unique identifier for the product
  3. UserId - unqiue identifier for the user
  4. ProfileName
  5. HelpfulnessNumerator - number of users who found the review helpful
  6. HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not
  7. Score - rating between 1 and 5
  8. Time - timestamp for the review
  9. Summary - brief summary of the review
  10. Text - text of the review  
  
## Objective:

The main objective for this analysis is to train a model which can seperate the postive and negative reviews.The Score column shows whether the review is positive or negative.  So for this problem, the main focus is on the Review text. The text is the most important feature. Based on the review text, a prediction model and determine if a future review is positive or negative, is built.

## Methodology:

  1. Data Pre-processing
  2. Data Cleaning
  3. Machine Learning Models
  
### 1.Data Pre-processing

  1. Classify a review to be positive if and only if the corresponding Score for the given review is 4 or 5.
  2. Classify a review to be negative if and only if the corresponding Score for the given review is 1 or 2.
  3. Ignore the reviews which has a Score rating of 3. Because 3 can be thought of as a neutral review. It's neither positive nor negative.
  4. Remove the duplicate entries from the dataset.
  5. Train the final model using four featurizations -> bag of words model, tf-idf model, average word-to-vec model and tf-idf weighted word-to-vec model.
  6. So at end of the training, the model will be trained on the above four featurizations to determine if a given review is positive or negative (Determining the sentiment polarity of the Amazon reviews).
  
### 2.Data Cleaning

  * Remove duplicate data points from the original dataset.
  * Remove URLs from text.
  * Remove HTML tags from all the reviews.
  * Remove words with numbers.
  * Remove punctuations from all the reviews.
  
### 3.Machine Learning Models
 
  * KNN
  * Logistic Regression
  
## Conclusion:

  * Positive reviews are very common.
  * Positive reviews are shorter.
  * Longer reviews are more helpful.
  * Despite being more common and shorter, positive reviews are found more helpful.
  * Frequent reviewers are more discerning in their ratings, write longer reviews, and write more helpful reviews.
  * Logistic Regression as a classification model performed the best result in classifying the reviews as compared to other classification models. Logistic Regression is able to find the best hyperplane which could sepearte the reviews into positive and negative.
  * I have also applied different models on all of the featurization techniques result, but i have found that logistic regression on tfidf performed the best result.
  * Metrics for evaluating logistic regression on tfidf are mentioned below:
  1. Accuracy : 89.53
  2. Precision : 0.96(positive) and 0.56(negative)
  3. Recall : 0.91(positive) and 0.78(negative)
  4. AUC : 0.93
  
 
