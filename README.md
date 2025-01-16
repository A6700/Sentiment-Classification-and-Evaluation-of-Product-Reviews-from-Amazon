# Sentiment-Classification-and-Evaluation-of-Product-Reviews-from-Amazon
This system is build upon 36547 reviews from Amazon with labeled sentiments ("positive" for 4 or 5 stars and "negative" for 1 or 2 stars) and aims to conduct sentiment classification of the reviews. The procedures consist of data preprocessing (including tokenization and an optional lemmaization section of irregular verbs to experiment with), building the baseline model and the classifier, and evaluations of the classifier.

# Content
1.   Data preprocessing.
      *   Tokenization (optional: experiment with lemmatization of irregular verbs).
      *   Compile the type list.
      *   Conduct the one-hot encoding.
      *   Compile the training dataset and the testing dataset.

2.   Set up the baseline and build the classifier.
      *   The baseline model: tokenized only by spaces.
      *   Model A-E: apply the adjusted data preprocessing methods.

3.   Evaluate the classifier.
      *   Compute the accuracy, precision, and recall value.
      *   Inspect the weights.

# Quick Start

You can use the following steps to train and test the sentiment classifier as well as evaluate the results.

## Download the repository and two ways to use the system

1.   Open [cl_sentiment_classifier.py](cl_sentiment_classifier.py) in your running environment.
