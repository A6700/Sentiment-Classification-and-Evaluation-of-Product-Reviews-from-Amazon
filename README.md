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

## Download the repository and two ways to implement the classifier

1.   Open [cl_sentiment_classifier.py](cl_sentiment_classifier.py) in your running environment.

2.   Open [CL_Sentiment_Classifier.ipynb](CL_Sentiment_Classifier.ipynb) in the [Google Colab](https://colab.research.google.com/).

## Instructions for setting up the baseline classifier

1.   Set up the baseline model by running the *The Baseline Model and Data Preprocessing* code block for data preprocessing and then *Build a Logistic Regression Model for Binary Classification of Sentiments* code block for building the baseline model.

2.   Run the *Evaluations of the Model* code block in order to retrive the results (accuracy, precision, and recall values) and to inspect weights.

## Instructions for building the classifier for later experiments

1.   Run the *Model A - E and Data Preprocessing* code block for data preprocessing.

     *   To experiment with the lemmatization of irregular verbs, you may first run the *Optional: experiment with the lemmatization of irregular verbs* code block and then uncomment the following lines in the *Model A - E and Data Preprocessing* code block:
       
         ```
         for s, t in enumerate(past_tense):
             if tokenized_reviews[i][j] == t:
                 tokenized_reviews[i][j] = verbs[s]
         for s, t in enumerate(past_participle):
             if tokenized_reviews[i][j] == t:
                 tokenized_reviews[i][j] = verbs[s]
         ```
     *   Then you are free to run the *Model A - E and Data Preprocessing* code block. (If you are skipping the lemmatization experiment, you can run the *Model A - E and Data Preprocessing* code block directly.)
       
2.   Run the *Build a Logistic Regression Model for Binary Classification of Sentiments* code block to build your classifier.
  
3.   Run the *Evaluations of the Model* code block in order to retrive the results (accuracy, precision, and recall values) and to inspect weights.

## Changing the parameters

1.   In *The Baseline Model and Data Preprocessing* and *Model A - E and Data Preprocessing*, find the following lines to change the vocabulary size of your `type_list`:

     ```
     type_list = so[0:5000]
     ```
     or
     ```
     type_list = so[0:1000]
     ```
     
2.   You can use the following command line to check the size of the compiled matrix:

     ```
     M.shape
     ```

3.   In *Build a Logistic Regression Model for Binary Classification of Sentiments*, you can switch the number of epochs and the learning rate with the following command lines:

     ```
     n_iters =
     lr =
     ```

# References

1.    [NLTK's list of english stopwords](https://gist.github.com/sebleier/554280)
