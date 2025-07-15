# 🚨 Sentiment Analysis of Tweets

This repository contains a sentiment analysis project that classifies tweets as disaster-related or not. Developed as part of a team collaboration at the University of Nebraska–Lincoln, this project explores multiple machine learning and deep learning approaches to natural language processing (NLP).

## 📌 Project Summary

The goal is to analyze short-form social media content (tweets) and identify whether they describe real emergencies. This is a binary classification problem approached using various machine learning models:

- **Multinomial Naive Bayes**
- **Word Sense Disambiguation (WSD) with Naive Bayes**
- **Recurrent Neural Networks (RNN)**

---

## 🧠 Techniques Used

### 🔍 Naive Bayes
- Used `CountVectorizer` for feature extraction
- Explored n-gram ranges and special tag replacements (e.g., replacing "@CNN" with "news")
- Achieved **~80% accuracy**

### 🧠 Word Sense Disambiguation (WSD)
- Used **NLTK** and **WordNet** for extracting word context
- Applied both NLTK and `scikit-learn` Naive Bayes implementations
- Achieved up to **79.8% accuracy**

### 🧠 Recurrent Neural Network (RNN)
- Implemented using **TensorFlow**
- Preprocessed tweets by removing stopwords, symbols, and padding to uniform length
- Built with embedding + RNN + dense layers
- Achieved **77% accuracy**

---

## 📊 Results Overview

| Model                   | Accuracy | Precision | Recall |
|------------------------|----------|-----------|--------|
| Naive Bayes (Bigram)   | 80%      | 81%       | 70%    |
| WSD (Sklearn NB)       | 79.8%    | 79.7%     | 71%    |
| RNN                    | 77%      | 80%       | 64%    |

- **F1 Score (RNN):** 77%
- Bayesian models performed slightly better due to limited dataset size and simpler structure.

---

## 📁 Dataset

- Total tweets: ~10,766  
  - **Training:** 7,503 tweets (43% disaster-related)
  - **Testing:** 3,263 tweets
- Each tweet contains:
  - Text
  - Optional keyword
  - Location

> Note: Location and keywords were excluded from most models.

---

## 🛠 Tools & Libraries

- Python
- Scikit-learn
- NLTK
- TensorFlow
- WordNet
- Pandas, NumPy

---

## 🔮 Future Work

- Improve preprocessing: better tokenization, handle slang, hashtags, emojis, etc.
- Use pre-trained language models
- Expand dataset for better generalization
- Optimize RNN layers and hyperparameters for deeper performance gains

---

