# 📰 Fake News Detection using Machine Learning (NLP Project)

This project is a **Natural Language Processing (NLP)** based classification system that detects whether a news article is **Fake or Real** using Machine Learning models.

We use **TF-IDF vectorization** and compare two models:
- Logistic Regression
- Support Vector Machine (SVM)

---

# 🚀 Project Objective

The goal of this project is to:
- Automatically classify news articles as Fake or Real
- Apply NLP techniques for text preprocessing
- Compare ML models for best performance

---

# 📊 Dataset Information

The dataset contains:

| Column | Description |
|---|---|
| title | Headline of the news |
| text | Full news content |
| label | 0 = Fake, 1 = Real |

---

# 🧹 Data Preprocessing

The following preprocessing steps were applied:

- Converted text to lowercase
- Removed punctuation
- Removed extra spaces
- Removed stopwords
- Combined `title + text` into a single feature (`content`)

<br>
# Model Performance Comparison

# Logistic Regression Results
## Accuracy: 0.9512 (95.12%)

-Class 0 (Fake):
-Precision: 0.94
-Recall:    0.96
-F1-score:   0.95

-Class 1 (Real):
-Precision: 0.96
-Recall:    0.94
-F1-score:   0.95

# Support Vector Machine (SVM) Results
## Accuracy: 0.9686 (96.86%)

-Class 0 (Fake):
-Precision: 0.96
-Recall:    0.97
-F1-score:   0.97

-Class 1 (Real):
-Precision: 0.98
-Recall:    0.96
-F1-score:   0.97

```python id="pre1"
df['content'] = df['title'] + " " + df['text']
