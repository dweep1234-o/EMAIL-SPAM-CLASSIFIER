# 📧 Email Spam Classifier

A machine learning project to automatically classify emails/messages as **spam** or **ham (legitimate)** using NLP and supervised learning.

---

## Problem Statement

Email communication is a primary medium for personal and professional correspondence, yet a significant portion of emails received are unsolicited spam — including phishing attempts, advertisements, and malicious content. Manual identification of spam is time-consuming and error-prone, while rule-based filters often fail to adapt to evolving spam tactics.

This project builds an **automated email spam classifier** using machine learning techniques to accurately distinguish between spam and legitimate emails. By training on labeled datasets, the model learns linguistic and structural patterns characteristic of spam, enabling real-time classification with high precision and recall.

---

## Dataset

**SMS Spam Collection Dataset**
- Source: UCI Machine Learning Repository / Kaggle
- Size: 5,572 messages
- Labels: `ham` (4,825) | `spam` (747)
- No download or API key required — loaded directly via URL in the notebook

---

## Project Pipeline

```
Raw Text → Preprocessing → TF-IDF Vectorization → Model Training → Evaluation → Prediction
```

1. **Dataset Loading & Exploration**
2. **Exploratory Data Analysis (EDA)** — class distribution, message length, word clouds
3. **Text Preprocessing** — lowercasing, URL/number removal, stopword removal, lemmatization
4. **Feature Engineering** — TF-IDF with unigrams + bigrams (5,000 features)
5. **Model Training** — Naive Bayes, Logistic Regression, SVM (LinearSVC)
6. **Evaluation** — accuracy, precision, recall, F1, confusion matrices
7. **Prediction** — custom input classification

---

## Models & Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Naive Bayes | ~97% | ~97% | ~93% | ~95% |
| Logistic Regression | ~98% | ~98% | ~95% | ~97% |
| SVM (LinearSVC) | ~98% | ~98% | ~96% | ~97% |

> Results may vary slightly due to random state and train/test split.

---

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3 |
| NLP | NLTK, TF-IDF |
| ML | Scikit-learn |
| Visualization | Matplotlib, Seaborn, WordCloud |
| Environment | Google Colab |

---

## How to Run

1. Open `email_spam_classifier.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Go to **Runtime → Run All**
3. All dependencies are installed automatically in the first cell

---

## File Structure

```
📁 internship/
├── email_spam_classifier.ipynb   # Main Colab notebook
└── README.md                     # Project documentation
```

---

## Key Findings

- Spam messages are significantly **longer** and contain more words than ham
- Common spam indicators: `free`, `win`, `claim`, `prize`, `click`, `urgent`
- TF-IDF with bigrams captures phrase-level patterns (e.g., "call now", "free prize")
- All three models exceeded **97% accuracy**; SVM and Logistic Regression edge out Naive Bayes on the minority spam class

---

## Possible Extensions

- Deep learning approaches: LSTM, BERT for contextual understanding
- Additional features: sender domain, capitalization ratio, link count
- Deployment as a REST API using Flask or FastAPI
- Real-time Gmail integration via Gmail API

---

## Author

**Dweep**
