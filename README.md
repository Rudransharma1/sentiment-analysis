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
VADER is a rule-based sentiment analysis tool designed for quick polarity
classification.

### Why VADER?
- Fast baseline model
- Works well for short reviews
- No training required

### Steps
- Applied VADER compound polarity scores
- Classified reviews as positive or negative
- Evaluated using confusion matrix

### Results
- Accuracy: ~76%
- High precision, moderate recall
- Struggles with complex sentence context

---

## Model 2: LSTM (Deep Learning)
LSTM was used to capture contextual and sequential patterns in customer reviews.

### Why LSTM?
- Handles long-term dependencies
- Better understanding of negations and context
- Suitable for NLP tasks

### Steps
- Text vectorization (Bag of Words + Tokenization)
- Sequence padding
- LSTM model with embedding and dropout layers
- Binary sentiment classification

### Results
- Test Accuracy: ~81%
- Better performance than VADER
- Improved handling of complex reviews

---

## Model Comparison
| Model | Accuracy | Strength |
|------|---------|----------|
| VADER | ~76% | Fast, simple baseline |
| LSTM | ~81% | Better contextual understanding |

---

## Key Insights
- Customer sentiment is nearly balanced
- Deep learning outperforms rule-based NLP
- Dataset size limits generalization
- Proper preprocessing significantly improves results

---

## Project Files
- Notebook: Sentiment_Analysis_Group06.ipynb
- HTML Output: Sentiment_Analysis_Group06.html
- Report: Group-6-Sentiment_Analysis.pdf
- Presentation: SENTIMENT ANALYSIS PRESENTATION.pdf
- Dataset: sentiment_train.csv

---

## Future Improvements
- Train on larger datasets
- Add transformer models (BERT)
- Deploy model as an API or dashboard
