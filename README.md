![project_pic.jpeg](project_pic.jpeg)

# Text Emotion Recognition Model 🤖

This project focuses on detecting emotions (fear, anger, joy, and sadness) from text data collected from Reddit. The model classifies each piece of text into one of the four emotion classes. The goal is to compare the performance of an LSTM-based model, DistilBERT, and RoBERTa for this task by computing Accuracy and F1-score.

# Project Overview

## Data Collection:

The dataset contains Reddit posts extracted via the reddit api and labeled with emotions: joy, anger, fear, and sadness.
Preprocessing steps include tokenization, stopword removal, stemming, and encoding with Tf-idf Vectorizer for the LSTM Model. The DistilBERT and RoBERTa models had minimal preprocessing (only lowercasing and special character removal).

## Models Implemented:

LSTM: A Bidirectional LSTM with embeddings generated using Tf-idf Vectorizer.

DistilBERT: A transformer model fine-tuned on the dataset.

RoBERTa: Another transformer model fine-tuned on the dataset.

## Evaluation Metrics:

Accuracy and F1-Score are computed for all models to compare performance.

## Data Preprocessing

The data is preprocessed using the following steps:

- Convert all text to lowercase.
- Remove special characters and stopwords.
- Apply stemming to normalize the words only for the LSTM model.
- Encode the data using Tf-idf Vectorizer for the LSTM model.


## LSTM Model Architecture:
- Embedding layer (using Tf-idf Vectorizer)
- Bidirectional LSTM
- Dropout Layer
- Layer Normalization
- Fully connected layer 
- Loss Function: CrossEntropyLoss
- Optimizer: AdamW
- Metrics: Accuracy, F1-Score

## DistilBERT and RoBERTa Models Architecture:
- Pre-trained transformer models
- Fine-tuned for emotion classification
- Loss Function: CrossEntropyLoss
- Optimizer: AdamW
- Metrics: Accuracy, F1-Score

## Performance

The models' performances were evaluated based on Accuracy and F1-Score. 
- The LSTM Model acheived an accuracy of 26% and an f1-score of 0.26
- The DistilBERT Model acheived an accuracy of 75% and f1-score of 0.74
- The RoBERTa Model achevied an accuracy of 80% and an f1-score of 0.80

## Conclusion

This project provided valuable insights into the complexities of data collection and preprocessing, deepening my understanding of these critical stages in machine learning. It also allowed me to enhance my skills in building Neural Networks, while highlighting the challenges involved in optimizing model performance. Through this experience, I gained a deeper appreciation for transfer learning and the benefits of leveraging pretrained models. Overall, the project gave me a solid grasp of how to select the most suitable models for various use cases.