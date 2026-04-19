# 🧠 NLP Text Vectorization: BoW & TF-IDF

This repository demonstrates two fundamental techniques used in **Natural Language Processing (NLP)** to convert text into numerical features:

* **Bag of Words (BoW)**
* **TF-IDF (Term Frequency - Inverse Document Frequency)**

These are essential preprocessing steps for building machine learning models on text data.

---

## 📂 Project Structure

```
.
├── BOW.md        # Explanation of CountVectorizer (Bag of Words)
├── TF_IDF.md     # Explanation of TfidfVectorizer (TF-IDF)
└── README.md     # Project overview (this file)
```

---

## 📘 Topics Covered

### 1. 🟦 Bag of Words (BoW)

* Converts text into **word frequency vectors**
* Ignores grammar and word order
* Simple and fast baseline technique

📄 Detailed explanation:
👉 [BOW.md](./BOW.md)

---

### 2. 🟩 TF-IDF

* Assigns **importance scores** to words
* Reduces weight of common words
* Highlights meaningful and rare terms

📄 Detailed explanation:
👉 [TF_IDF.md](./TF_IDF.md)

---

## ⚖️ BoW vs TF-IDF

| Feature     | Bag of Words    | TF-IDF                       |
| ----------- | --------------- | ---------------------------- |
| Output      | Raw counts      | Weighted scores              |
| Importance  | All words equal | Rare words get higher weight |
| Performance | Basic           | More effective for NLP tasks |

---

## 🚀 Why This Matters

Machine learning models cannot understand raw text.
These techniques transform text into numerical form so models can process it.

Used in:

* Text classification
* Sentiment analysis
* Spam detection
* Search engines

---

## ⚙️ Requirements

```bash
pip install scikit-learn pandas
```

---


## 👨‍💻 Goal of This Repo

To build a **strong foundation in text vectorization**, which is the first step in almost every NLP pipeline.

---
