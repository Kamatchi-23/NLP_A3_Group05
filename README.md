# NLP_A3_Group05
This repository contains the code implementations along with the datasets for the Final NLP Group Project.\
Subject Code: 42850\
Team Member Details:
1. Dayu Zhao
2. Kamatchi Gnanavel
3. Vandana Sreenivasan  
4. Zhuoqian Pan

## Project Aim:
The purpose of this project is to examine the different NLP models for the purpose of analyzing the mental health state and predicting the different types of emotion expressed on Social Media platforms by the users. For this reason, we have taken the Twitter dataset from the Hugging Face platform, containing around 5.05k labeled data records split between train, test and validation sets with four classes of emotions:\ 
0-> anger\
1-> joy\
2-> optimism\
3-> sadness

## Dataset:
Twitter eval emotion dataset from Hugging Face
Link: https://huggingface.co/datasets/tweet_eval 

## Models Explored:
1. Linear Support Vector Classifier (SVC)
2. Bidirectional Long-Short Term Memory (BiLSTM)
3. BERT
4. RoBERTa
5. DistilBERT
   
## Proposed Solution:
Text Processing Steps using text_hammer include:
1.   Changing to lower case
2.   Expanding words like you're to you are, i'm to I am
3.   Removing emails
4.   Removing HTML tags
5.   Removing special characters like @, #, % etc
6.   Removing accented characters like u^, `a etc

DistilBERT with the following hyperparameters:
•	learning_rate: 1e-5\
•	batch_size: 64\
•	decay: 1e-8\
•	optimizer: Adam\
•	epochs: 12

## Test Data Results Achieved:
1. F1 score: 0.7917
2. Accuracy: 0.7952

## Contribution Towards Code Implementation:
1. Kamatchi Gnanavel - implemented NLP_A3_final_implementation.ipynb and StopWords_removed_implementation.ipynb
2. Vandana Sreenivasan - implemented SVM_and_BERT_Sentiment_analysis_nlp.ipynb

## File Details:
1. SVM_and_BERT_Sentiment_analysis_nlp.ipynb - presents the exploration and implementation of the two models - SVM and BERT.
2. NLP_A3_final_implementation.ipynb - presents the final implementation of the five overall models along with the test and custom data results
3. StopWords_removed_implementation.ipynb - presents the code and results for the five models where the text preprocessing steps included lemmatization and stop words removal. This is an experimental implementation to see the difference in model performance with the text preprocessing steps. It was observed that performance was slightly lower with stop words removed which could be attributed to the loss of data with stop words removed from short pieces of texts such as tweets, where the given dataset contained maximum length of tweets to be containing 33 words even without basic cleaning.
