# NLP-Disaster-Tweets-Kaggle-Project
Overview
This project builds a model to classify tweets as either related to real disasters or not. The dataset is from a Kaggle competition and includes tweets labeled as 1 (disaster) or 0 (not disaster). I wanted to see how well an LSTM-based model could learn these patterns from text.

Dataset
Train set: 7,613 tweets

Test set: 3,263 tweets

Each tweet includes a text, optional keyword, optional location, and a target label in the train set.

Main Steps
Performed EDA to understand text length, common keywords, location breakdowns, etc.

Cleaned the tweets (lowercasing, removing URLs, hashtags, punctuation, stopwords).

Tokenized and padded sequences for model input.

Built two models:

A basic LSTM

A more complex Bidirectional LSTM

Results
The basic LSTM performed poorly (57% accuracy), stuck around random guessing.

The Bidirectional LSTM reached around 79% validation accuracy with tuning.

Best configuration: batch_size=16, learning_rate=0.0005

Reflection
I learned that for this task, simpler models couldn’t capture enough information from the tweet text. Bidirectional LSTM worked much better by using context from both directions. Still, the model missed a lot of disaster tweets, which would be risky in a real-world use case.
