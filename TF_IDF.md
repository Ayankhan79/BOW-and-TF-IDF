# 🧠 TF-IDF Text Vectorization using TfidfVectorizer

This project demonstrates how to convert text data into numerical form using **TF-IDF (Term Frequency - Inverse Document Frequency)** with `TfidfVectorizer`.

---

## 🚀 Overview

Unlike simple word counting, TF-IDF assigns importance to words based on:

* How frequently they appear in a sentence (TF)
* How rare they are across all sentences (IDF)

This helps highlight meaningful words and reduce the impact of common ones.

---

## 📂 Code

```python
from sklearn.feature_extraction.text import TfidfVectorizer
import pandas as pds

A1 = 'hello and welcome dosto'
A2 = 'shri love NLP'
A3 = 'shri is good boy'

vectorizer = TfidfVectorizer(stop_words='english')
vectors = vectorizer.fit_transform([A1, A2, A3])

feature_names = vectorizer.get_feature_names_out()
dense = vectors.todense()

result = pds.DataFrame(dense, columns=feature_names)

print(result)
```

---

## 🔍 How It Works

### 1. Input Sentences

```
A1: hello and welcome dosto  
A2: shri love NLP  
A3: shri is good boy
```

---

### 2. Stopword Removal

Common words like **"and"**, **"is"** are removed.

---

### 3. Vocabulary

```
boy, dosto, good, hello, love, nlp, shri, welcome
```

---

### 4. TF-IDF Calculation

Each word gets a score:

* Higher score → more important
* Lower score → more common

---

### 5. Output Example

| Sentence | boy  | dosto | good | hello | love | nlp  | shri | welcome |
| -------- | ---- | ----- | ---- | ----- | ---- | ---- | ---- | ------- |
| A1       | 0.00 | 0.58  | 0.00 | 0.58  | 0.00 | 0.00 | 0.00 | 0.58    |
| A2       | 0.00 | 0.00  | 0.00 | 0.00  | 0.58 | 0.58 | 0.58 | 0.00    |
| A3       | 0.58 | 0.00  | 0.58 | 0.00  | 0.00 | 0.00 | 0.44 | 0.00    |

*(Values are approximate)*

---

## 📌 Key Concepts

* **TF (Term Frequency)**
  Measures how often a word appears in a document.

* **IDF (Inverse Document Frequency)**
  Reduces importance of common words across documents.

* **TF-IDF Score**
  Combines both to give meaningful word importance.

---

## ⚙️ Requirements

```bash
pip install scikit-learn pandas
```

---

## 💡 Use Cases

* Search engines (ranking relevance)
* Document similarity
* Text classification
* Keyword extraction

---

## 👨‍💻 Author

A simple NLP project to understand TF-IDF vectorization and its advantages over basic word counting.

---
