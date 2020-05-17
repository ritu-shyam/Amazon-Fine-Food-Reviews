# Amazon-Fine-Food-Reviews
This repository contains a series of experiments performed on the Amazon Reviews dataset.This includes data visualization techniques,NLP related tasks,and prediction by various machine learning models.

The dataset can be downloaded from : https://www.kaggle.com/snap/amazon-fine-food-reviews

Basic information about the downloaded dataset

  Number of reviews: 568,454
  Number of users: 256,059
  Number of products: 74,258
  Timespan: Oct 1999 - Oct 2012
  Number of Attributes/Columns in data: 10
  
Attribute Information:

  1.Id
  2.ProductId - unique identifier for the product
  3.UserId - unqiue identifier for the user
  4.ProfileName
  5.HelpfulnessNumerator - number of users who found the review helpful
  6.HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not
  7.Score - rating between 1 and 5
  8.Time - timestamp for the review
  9.Summary - brief summary of the review
  10.Text - text of the review  
  
Objective:

The main objective for this analysis is to train a model which can seperate the postive and negative reviews.The Score column shows whether the review is positive or negative.  So for this problem, the main focus is on the Review text. The text is the most important feature. Based on the review text, a prediction model and determine if a future review is positive or negative, is built.

Methodology:

  1.Data Pre-processing
  2.Data Cleaning
  3.Machine Learning Models
  
1.Data Pre-processing

  (a)Classify a review to be positive if and only if the corresponding Score for the given review is 4 or 5.
  (b)Classify a review to be negative if and only if the corresponding Score for the given review is 1 or 2.
  (c)Ignore the reviews which has a Score rating of 3. Because 3 can be thought of as a neutral review. It's neither positive nor            negative.
  (d)Remove the duplicate entries from the dataset.
  (e)Train the final model using four featurizations -> bag of words model, tf-idf model, average word-to-vec model and tf-idf weighted      word-to-vec model.
  (f)So at end of the training, the model will be trained on the above four featurizations to determine if a given review is positive or      negative (Determining the sentiment polarity of the Amazon reviews).
  
2.Data Cleaning

  (a)Remove duplicate data points from the original dataset.
  (b)Remove URLs from text.
  (c)Remove HTML tags from all the reviews.
  (d)Remove words with numbers.
  (e)Remove punctuations from all the reviews.
  
3.Machine Learning Models
 
  (a)KNN
  (b)Logistic Regression
 
 
