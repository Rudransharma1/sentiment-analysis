![Project Cover](COVER.jpg)

# Sentiment Analysis – Restaurant Reviews

## Project Description
This project builds an end-to-end sentiment analysis pipeline on restaurant review
text to classify sentiment as **Positive** or **Negative**. The goal is to transform
unstructured customer feedback into measurable insights that support business
decisions such as service improvement, complaint tracking, and customer experience
monitoring.

The project compares a **rule-based NLP approach (VADER)** with a
**deep learning model (LSTM)** to demonstrate model selection and trade-offs.

---

## Project Structure
All project files are currently stored in the repository root:


---

## Access Project Files

- 📊 **Dataset**  
  [sentiment_train.csv](sentiment_train.csv)

- 📓 **Jupyter Notebook**  
  [Sentiment_Analysis_Group06.ipynb](Sentiment_Analysis_Group06.ipynb)

- 🌐 **HTML Output**  
  [Sentiment_Analysis_Group06.html](Sentiment_Analysis_Group06.html)

- 📄 **Final Report (PDF)**  
  [Group-6-Sentiment_Analysis.pdf.pdf](Group-6-Sentiment_Analysis.pdf.pdf)

- 📊 **Presentation**  
  [SENTIMENT_ANALYSIS_PRESENTATION.pdf.pdf](SENTIMENT_ANALYSIS_PRESENTATION.pdf.pdf)

---

## Step 1 — Define the Problem
**Goal:** Predict customer sentiment from review text.  
**Business Value:** Automatically summarize customer opinions at scale instead of
manual review analysis.

---

## Step 2 — Data Understanding
- Dataset: Restaurant reviews with sentiment labels
- Target column: `Polarity`
  - `0` = Negative
  - `1` = Positive
- Text column: `Sentence`

**Data checks performed:**
- Verified schema and label definitions
- Checked for missing values and duplicates
- Confirmed sentiment class distribution

---

## Step 3 — Data Cleaning & Text Preprocessing
Text preprocessing was performed to prepare data for modeling:

- Converted text to lowercase
- Removed extra spaces and unwanted characters
- Tokenized text into individual words
- Removed stopwords while preserving negations (e.g., *not*, *never*)
- Applied normalization where appropriate

**Output:** Cleaned text ready for feature extraction and modeling.

---

## Step 4 — Exploratory Data Analysis (EDA)
EDA was used to validate data quality and sentiment behavior:

- Sentiment distribution analysis
- Identification of common word patterns
- Sanity checks to ensure data suitability for modeling

**Why this matters:** Prevents training models on biased or low-quality data.

---

## Step 5 — Baseline Model (VADER Sentiment Analyzer)
A fast baseline model was implemented using **VADER**.

**Why VADER:**
- No training required
- Provides quick benchmark results
- Effective for short text reviews

**Process:**
- Computed polarity scores
- Converted scores to sentiment labels
- Compared predictions with true labels

**Evaluation:**
- Confusion matrix
- Accuracy, precision, and recall

---

## Step 6 — Deep Learning Model (LSTM)
An **LSTM** model was trained to capture sequential and contextual information.

**Why LSTM:**
- Learns word order and context
- Handles negations and longer reviews better

**Process:**
- Text vectorization and tokenization
- Sequence padding
- LSTM model with embedding and dropout layers
- Prediction on test data

**Evaluation:**
- Test accuracy
- Confusion matrix
- Comparison with VADER results

---

## Step 7 — Model Comparison & Findings
**Summary:**
- **VADER:** Fast and simple but struggles with complex language
- **LSTM:** Higher accuracy and better contextual understanding

**Why comparison matters:** Demonstrates analytical thinking and model selection skills.

---

## Step 8 — Outputs & Documentation
To ensure transparency and reproducibility, the repository includes:
- Jupyter notebook with full workflow
- HTML output for easy viewing
- PDF report with detailed documentation
- Presentation summarizing business insights
- Dataset used in analysis

---

## Step 9 — Reproducibility (How to Run)
1. Open `Sentiment_Analysis_Group06.ipynb`
2. Ensure `sentiment_train.csv` is in the same directory
3. Run cells top-to-bottom to reproduce:
   - Data preprocessing
   - EDA
   - VADER baseline
   - LSTM training
   - Model evaluation

---

## Step 10 — Future Improvements
- Train on larger and more diverse datasets
- Improve handling of sarcasm and irony
- Add transformer-based models (e.g., BERT)
- Deploy as a web application or API for real-time sentiment analysis

---

The insights generated from this project help businesses identify customer pain
points, monitor service quality, and prioritize improvements using real-world
customer feedback.

