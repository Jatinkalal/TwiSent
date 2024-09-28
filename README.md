# TwiSent : Tweet Based Public Sentiment Analysis of The New Education Policy (NEP) 2020

## Introduction
This project uses sentiment analysis to classify public tweets about the New Education Policy (NEP) 2020 as positive, negative, or neutral. Unlike classical machine learning methods, our LSTM-based approach captures contextual meaning in longer text sequences, offering more accurate results. The model is tested on the NEP 2020 dataset [availble on Kaggle](https://www.kaggle.com/datasets/rishabh6377/india-national-education-policy2020-tweets-dataset)

## System Architecture
![archi](https://github.com/Jatinkalal/TwiSent/blob/main/Images/Architecture.png)
This figure illustrates the architecture of a sentiment analysis model for raw input tweet. The process begins with a Pre-processing module, consisting of
standard pre-processing steps and tokenization, followed by polarity assignment. The processed tweet is converted into dense vector representation with
specified dimension (Nx100). This vector represented tweet is then fed into an LSTM layer, which is designed to understand the sequence and context of the
words. Finally, the output from the LSTM layer is passed through a softmax layer, which classifies the sentiment of the text into positive (POS), neutral
(NEU), or negative (NEG).

## Pre Processing of dataset
![preprocess](https://github.com/Jatinkalal/TwiSent/blob/main/Images/Preprocessing.png)
The preprocessing unit takes in raw input tweet and . Then we
remove the stop words to arrive at only meaningful words which provide
context to our sentences, we then index each word.

## Distribution of dataset into repeating and non repeating tweets
![distrbution](https://github.com/Jatinkalal/TwiSent/blob/main/Images/RepeatvsNon.png)
The public tweets are repeated in the dataset because each retweet is also considered as a new independent tweet irrespective of the content owing to different tweet id posted.

## Labelling of dataset
![vaderbro](https://github.com/Jatinkalal/TwiSent/blob/main/Images/DistributionVader.png)
Distribution of the dataset by labelling each tweet into positive, negative and neutral by using Valence Aware Dictionary and Sentiment
Reasoner (VADER), similar distribution was observed for labelling using TextBlob.

## Results for model trained on TextBlob
![Res](https://github.com/Jatinkalal/TwiSent/blob/main/Images/TextblobRes.png)
The confusion matrix depicts the prediction of the model using all tweets labelled by TextBlob tested on 60 custom input tweets.










