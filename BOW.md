# 🧠 Bag of Words Text Vectorization (CountVectorizer)

This project demonstrates how to convert text data into numerical format using the **Bag of Words (BoW)** technique with `CountVectorizer` from `scikit-learn`.

---

## 🚀 Overview

Natural Language Processing (NLP) models cannot directly understand raw text.
So, we convert text into numbers.

This project:

* Takes multiple sentences as input
* Removes common English stopwords
* Builds a vocabulary
* Converts each sentence into a vector of word frequencies
* Displays the result in a structured table using `pandas`

---

## 📂 Code

```python
from sklearn.feature_extraction.text import CountVectorizer
import pandas as pd

A1 = 'hello and welcome dosto' 
A2 = 'shri love NLP' 
A3 = 'shri is good boy'

vectorizer = CountVectorizer(stop_words='english')
vectors = vectorizer.fit_transform([A1, A2, A3])

feature_names = vectorizer.get_feature_names_out()
dense = vectors.todense()

result = pd.DataFrame(dense, columns=feature_names)

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

### 2. Stopword Removal

Words like **"and"**, **"is"** are removed automatically.

---

### 3. Vocabulary Creation

The model extracts unique words:

```
boy, dosto, good, hello, love, nlp, shri, welcome
```

---

### 4. Vector Representation

Each sentence is converted into a vector:

| Sentence | boy | dosto | good | hello | love | nlp | shri | welcome |
| -------- | --- | ----- | ---- | ----- | ---- | --- | ---- | ------- |
| A1       | 0   | 1     | 0    | 1     | 0    | 0   | 0    | 1       |
| A2       | 0   | 0     | 0    | 0     | 1    | 1   | 1    | 0       |
| A3       | 1   | 0     | 1    | 0     | 0    | 0   | 1    | 0       |

---

## 📌 Key Concepts

* **Bag of Words (BoW)**
  Ignores grammar and word order, focuses only on word frequency.

* **CountVectorizer**

  * Converts text → numerical vectors
  * Automatically lowercases words
  * Removes stopwords (if specified)

* **Sparse Matrix**
  Efficient storage for large text data (converted to dense here for readability).

---

## ⚙️ Requirements

Install dependencies:

```bash
pip install scikit-learn pandas
```

---

## 💡 Use Cases

* Text classification
* Sentiment analysis
* Spam detection
* Feature engineering for ML models

---

## 🔮 Next Steps

You can extend this by:

* Using **TF-IDF Vectorizer**
* Adding **n-grams (bigrams, trigrams)**
* Training ML models on this data

---

## 👨‍💻 Author

Created as a beginner-friendly NLP project to understand text vectorization.

---
