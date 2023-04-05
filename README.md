# Twitter-Sentiment-Analysis
Sentiment analysis also referred to as opinion mining, is an approach to natural language processing that identifies the emotional tone behind a body of text. 

This project performs sentiment analysis on tweets related to Thanksgiving, using a dataset obtained from Twitter API. The dataset is in CSV format and is loaded into an Amazon S3 bucket via Amazon Kinesis Data Firehose. A machine learning pipeline is created to train a Logistic Regression model for supervised sentiment analysis, and the accuracy of the model is calculated. Finally, the prediction data is written to a personal S3 bucket for further analysis.

## Dataset

The dataset used in this project is obtained from Twitter API and is in CSV format. The dataset contains tweets related to Thanksgiving, which are used for sentiment analysis. The dataset is loaded into an Amazon S3 bucket via Amazon Kinesis Data Firehose, which allows for easy data ingestion and storage.

## Machine Learning Pipeline

The machine learning pipeline consists of the following steps:

1. Data Preprocessing: The tweets in the dataset are preprocessed to remove any irrelevant information, such as URLs, special characters, and emojis. Text normalization techniques, such as tokenization, stopword removal, and stemming/lemmatization, are applied to clean the text data.

2. Feature Extraction: The cleaned text data is transformed into numerical features using techniques such as bag-of-words or term frequency-inverse document frequency (TF-IDF) vectorization. These numerical features are used as input to the machine learning model.

3. Model Training: A Logistic Regression model is trained using the preprocessed and transformed data. The model is trained on a labeled dataset with sentiment labels (positive, negative, or neutral) for each tweet.

4. Model Evaluation: The accuracy of the trained model is calculated using appropriate evaluation metrics, such as accuracy, precision, recall, and F1-score. This helps to assess the performance of the model and determine its effectiveness in sentiment analysis.

5. Prediction: The trained model is used to predict the sentiment of new, unseen tweets related to Thanksgiving. The prediction results are written to a personal S3 bucket for further analysis or visualization.

## Prerequisites

To run this project, you need to have the following prerequisites:

- Access to Twitter API to obtain the dataset
- An Amazon EC2 Instance to deploy the project
- An Amazon S3 bucket to store the dataset and prediction results
- Knowledge of machine learning techniques, particularly Logistic Regression
- Python programming skills to implement the machine learning pipeline

## Usage

To use this project, follow these steps:

1. Obtain the Twitter dataset in CSV format using the Twitter API.
2. Load the dataset into an Amazon S3 bucket using Amazon Kinesis Data Firehose.
3. Preprocess the dataset by cleaning the text data and transforming it into numerical features.
4. Train a Logistic Regression model using the preprocessed data.
5. Evaluate the accuracy of the trained model using appropriate evaluation metrics.
6. Use the trained model to predict the sentiment of new tweets related to Thanksgiving.
7. Write the prediction results to a personal S3 bucket for further analysis or visualization.
