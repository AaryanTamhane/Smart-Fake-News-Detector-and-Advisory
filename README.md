# 📰 Fake News, Spam, and Sentiment Detection System

A Machine Learning-based project to detect fake or spam news, analyze its sentiment, and provide smart advisory suggestions for responsible content sharing.

---

## 📂 Project Overview

This project uses Natural Language Processing (NLP) and Machine Learning (ML) to:
- Classify news as Fake, Real, or Spam
- Analyze the emotional tone (Sentiment)
- Provide advisory messages to users before sharing content

---

## 🚀 What It Does

✅ Loads and merges multiple datasets (Fake, Real, Spam)  
✅ Cleans and preprocesses text (lowercasing, stopwords, stemming, etc.)  
✅ Converts text into TF-IDF vectors  
✅ Trains ML models like Naive Bayes to classify news  
✅ Uses VADER for sentiment analysis (Positive / Neutral / Negative)  
✅ Gives a final advisory like:
- “Avoid sharing”
- “Fact-check before forwarding”
- “Safe to engage”

---

## 🛠️ How It Works

### 🟦 Part 1: Dataset Integration & Preprocessing
- Load datasets: `Fake.csv`, `True.csv`, `spam.csv`
- Label each dataset (Fake, Real, Spam)
- Merge datasets into one
- Preprocess text:
  - Lowercasing
  - Removing punctuation/symbols
  - Tokenization
  - Stopword removal
  - Stemming
- Store results in a new column: `clean_text`

### 🟩 Part 2: Feature Extraction & Model Training
- Use `TfidfVectorizer(max_features=5000)` to convert text to numbers
- Analyze top keywords using average TF-IDF scores
- Train classifier models:
  - Multinomial Naive Bayes (Fake/Real/Spam)
- Evaluate models with accuracy score, classification report

### 🟥 Part 3: Sentiment & Expert System Advisory
- Use VADER Sentiment to label articles as:
  - Positive / Neutral / Negative
- Define a rule-based advisory system:
  - Fake + Negative → “Avoid sharing”
  - Real + Positive → “Safe to engage”
- Final function:
  - Input text → Clean → Vectorize → Predict → Sentiment → Advisory

---

## 🧪 Sample Output
News: "Government offers free education to all students this year" Prediction: Real
Sentiment: Positive
Advisory: Safe to engage ✅

---

## 📁 Folder Structure

project/ ├── Data/ │ ├── Fake.csv │ ├── True.csv │ └── Spam.csv ├── Notebooks/ │ ├── Data_Preprocessing.ipynb │ ├── TFIDF_Model_Training.ipynb │ └── Sentiment_Advisory_System.ipynb ├── requirements.txt └── README.md

