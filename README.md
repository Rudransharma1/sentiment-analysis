![Project Cover](cover.png)

# Sentiment Analysis – Restaurant Reviews

## Overview
This project performs end-to-end sentiment analysis on restaurant reviews using
both a rule-based NLP model (VADER) and a deep learning model (LSTM).

---

## Dataset
- ~2,400 restaurant reviews
- Features:
  - Sentence (review text)
  - Polarity (0 = Negative, 1 = Positive)
- No missing values

Dataset file:
sentiment_train.csv

---

## Tools & Libraries
- Python
- Pandas, NumPy
- NLTK
- Scikit-learn
- TensorFlow / Keras

---

## Project Workflow

### 1. Data Preprocessing (COMMON FOR BOTH MODELS)
- Lowercasing text
- Removing special characters and numbers
- Tokenization
- Stopword removal (custom handling for negations like "not")
- Text normalization

---

## Model 1: VADER Sentiment Analysis
VADER is a rule-based sentiment anal
