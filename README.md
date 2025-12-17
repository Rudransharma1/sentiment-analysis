---

## Project Structure

All project files are organized as follows:

sentiment-analysis/
├── README.md
├── cover.jpg
│
├── data/
│   └── sentiment_train.csv
│
├── notebook/
│   └── Sentiment_Analysis_Group06.ipynb
│
├── output/
│   └── Sentiment_Analysis_Group06.html
│
├── reports/
│   ├── Group-6-Sentiment_Analysis.pdf
│   └── Project_Report_Big_Data.docx
│
└── presentation/
    └── SENTIMENT_ANALYSIS_PRESENTATION.pdf
## Access Project Files

- 📊 Dataset:  
  [sentiment_train.csv](data/sentiment_train.csv)

- 📓 Jupyter Notebook:  
  [Sentiment_Analysis_Group06.ipynb](notebook/Sentiment_Analysis_Group06.ipynb)

- 🌐 HTML Output:  
  [Sentiment_Analysis_Group06.html](output/Sentiment_Analysis_Group06.html)

- 📄 Final Report (PDF):  
  [Group-6-Sentiment_Analysis.pdf](reports/Group-6-Sentiment_Analysis.pdf)

- 📊 Presentation:  
  [SENTIMENT ANALYSIS PRESENTATION.pdf](presentation/SENTIMENT_ANALYSIS_PRESENTATION.pdf)

## Project Description
## Detailed Project Description (End-to-End)

This project builds an end-to-end sentiment analysis pipeline on restaurant review text to classify sentiment as **Positive** or **Negative**. The goal is to transform unstructured customer feedback into measurable insights that can support business decisions (service improvements, complaint tracking, and customer experience monitoring).

---

## Step 1 — Define the Problem
**Goal:** Predict sentiment from review text.  
**Business value:** Automatically summarize how customers feel at scale, instead of reading reviews manually.

---

## Step 2 — Data Understanding
**Dataset:** Restaurant reviews dataset (text + sentiment label).  
**Target column:** `Polarity`  
- `0` = Negative  
- `1` = Positive  

**Text column:** `Sentence` (review text)

**Data checks performed:**
- Confirmed dataset schema and label meaning
- Verified missing values and duplicates
- Verified sentiment class distribution (balance)

---

## Step 3 — Data Cleaning & Text Preprocessing
Text data is noisy, so preprocessing is required before modeling.

**Preprocessing steps included:**
- Convert text to lowercase
- Remove extra spaces, punctuation noise, and unwanted characters
- Tokenization (split text into words)
- Stopword removal (while keeping important negations like *not*, *never*)
- Optional normalization (lemmatization/stemming depending on the notebook)

**Output of this step:** cleaned text ready for feature extraction/model input.

---

## Step 4 — Exploratory Data Analysis (EDA)
The project validates the dataset and sentiment behavior before modeling.

**EDA steps included:**
- Sentiment distribution (positive vs negative)
- Basic text patterns (frequent words)
- Sanity checks that data is usable for training

**Why this matters:** prevents training a model on biased or low-quality data.

---

## Step 5 — Baseline Model (VADER Sentiment Analyzer)
A fast baseline was built using **VADER**, a rule-based NLP sentiment method.

**Why VADER was used:**
- No training required
- Provides quick benchmark performance
- Useful for short review text

**Process:**
- Compute polarity score for each review
- Convert score into predicted label (positive/negative)
- Compare predictions with true `Polarity`

**Evaluation:**
- Confusion matrix
- Accuracy, precision, recall (to understand trade-offs)

---

## Step 6 — Deep Learning Model (LSTM)
To better capture context and sequential meaning, an **LSTM** model was trained.

**Why LSTM was used:**
- Learns patterns from word order and context
- Handles negations and longer text better than rule-based approaches

**Process:**
- Convert text into numeric format (tokenization / sequences)
- Pad sequences for equal length input
- Train LSTM network with embedding + dropout layers
- Predict sentiment on test set

**Evaluation:**
- Test accuracy and performance metrics
- Confusion matrix
- Comparison with baseline VADER results

---

## Step 7 — Model Comparison & Findings
Both approaches were compared to show strengths and limitations.

**Summary:**
- **VADER**: Fast baseline, but struggles with nuanced/complex language
- **LSTM**: Higher accuracy and better context handling, but needs training and more compute

**Why comparison matters:** shows real analytical thinking and model selection skills.

---

## Step 8 — Outputs & Documentation
To make the project recruiter-friendly and reproducible, all outputs are included:
- Notebook with full code and workflow
- HTML output (easy viewing without running code)
- PDF report (formal documentation)
- Presentation (business-ready summary)
- Dataset stored in the repo for transparency

---

## Step 9 — Reproducibility (How to Run)
1. Open the notebook: `notebook/Sentiment_Analysis_Group06.ipynb`
2. Ensure dataset is available at: `data/sentiment_train.csv`
3. Run cells top-to-bottom to reproduce:
   - preprocessing
   - EDA
   - VADER baseline
   - LSTM training
   - evaluation results

---

## Step 10 — Future Improvements
- Train on a larger, more diverse dataset
- Improve text preprocessing and handle sarcasm/irony
- Add transformer-based models (BERT)
- Deploy as a web app / API for real-time sentiment scoring


The insights generated from this analysis can help restaurants identify customer
pain points, monitor service quality, and prioritize improvements based on
real customer feedback. This project demonstrates practical application of NLP
and deep learning techniques in a real-world business context.

