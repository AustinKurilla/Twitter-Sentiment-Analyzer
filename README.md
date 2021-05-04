# Twitter-Sentiment-Analyzer

In order to run you must create a config.py file containing : consumer_key +consumer_secret + access_token + access_token_secret, From the Twitter API

The first cell must be run every load
Running the second cell will retrain the NaiveBayesClassifier algorithm and save it into the pickle file (this cell does not need to be run since the pickle file is provided aleady and is loaded in the first cell)
The 3rd cell allows you to enter a search string and the sentiment of the search will be calculated using the trained NaiveBayesClassifier algorithm
The last cell allows you to enter a search string and the sentiment will be calculated using the sentimentIntenisityAnalysis algorthm, a pie chart and word clouds will also be displayed for tweets of positve, neutral, and negative sentiment. 

Our plan for our data mining project is to do social media sentiment analysis using Naive Bayes. We are going to use the NLKT python library for both the natural language processing and the classification of the data. Our plan is to train our model using a dataset of movie reviews. The dataset we are using is a set of 50k movie reviews posted on IMDB, the data consists of 2 columns, one column containing the review and another column containing the overall sentiment of the review. The data can be found here (https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) The words being used in the review will be associated with negative or positive sentiment based on if they are used more often in negative reviews or positive reviews. Using our model, we will classify social media posts on Twitter as either negative, neutral, or positive sentiment. based on if they use more negative words or positive words. Using the Twitter API, we will use GET requests to pull tweets relating to user input. For example, if a user wants to see the sentiment of 'Drake' we will request a set of tweets containing the word 'Drake', then using our model the words in each of the tweets will be analyzed then each tweet will be classified as negative, neutral, or positive sentiment. Based on if more tweets are considered positive, negative, or neutral the classifier will determine the overall sentiment of the topic. The classifier will report the overall sentiment as either very bad, bad, neutral, good, or very good. We may face are dealing with sarcasm, irony, and the context of a sentence when determining sentiment.


UPDATE:
Due to our trained naivebayesclassifer algorithm being very biased towards negative sentiment, there is a second part that uses sentimentIntensityAnalysis instead. 
