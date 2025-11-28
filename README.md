#  Email Phishing Detection Using Machine Learning & Deep Learning
A Complete End-to-End NLP & Cybersecurity Project

---

##  Project Overview

Phishing remains one of the most widely used cyber-attack methods. This project builds a powerful model capable of detecting phishing emails using both machine learning and deep learning techniques.

Using a cleaned dataset of 17,538 email samples, I developed multiple models from TF-IDF based ML classifiers to RNN architectures like LSTM, GRU, and Bidirectional LSTM achieving up to 98% accuracy.

---

##  Dataset Description

*Dataset:* Phishing_Email.txt

After cleaning:
- *17,538 valid records*
- Columns:
  - Email Text
  - Email Type (Safe Email / Phishing Email)

---

##  1. Data Cleaning & Preprocessing

### Steps Performed
- Removed irrelevant index column  
- Removed null values and duplicates  
- Cleaned email text (removed hyperlinks, punctuation, extra spaces)
- Converted text to lowercase  
- Encoded labels using LabelEncoder

The dataset contained noisy symbols and links typical of phishing messages.  
Cleaning significantly improved text quality and model performance.

---

## 2. Exploratory Data Analysis (EDA)

### Visualizations created:
- Bar chart showing distribution of Safe vs Phishing emails  
- Pie chart of class balance  
- WordClouds for frequent words  
- WordCloud of unique words
  
Phishing emails often contained promotional keywords like free, click, offer.  
Safe emails had more structured and formal vocabulary.

---

##  3. Feature Engineering

Two approaches were used:

### *A) TF-IDF Vectorization*  
- Maximum features: 10,000  
- Used for all classical ML models

### *B) Tokenization + Padding*  
- Sequence length: 150  
- Used for RNN-based Deep Learning models

TF-IDF produced excellent performance with linear models.  
Deep learning required tokenization to handle sequences effectively.

---

## 🧠 4. Machine Learning Models & Results

| Model | Accuracy | F1 Score | Comments |
|-------|----------|----------|----------|
| Naive Bayes | 97.52% | 97.99% | Fast and strong baseline |
| Logistic Regression | 97.95% | 98.34% | Consistent performance |
| *SGD Classifier* | *98.49%* | *98.77%* | ⭐ Best ML model |
| XGBoost | 96.61% | 97.26% | Slight overfitting |
| Decision Tree | 92.96% | 94.21% | Weak due to high variance |
| Random Forest | 97.83% | 98.23% | Robust ensemble method |
| MLP Classifier | 98.32% | 98.63% | Strong neural baseline |

The *SGD Classifier* performed best overall.  
Ensemble models and MLP showed strong stability and accuracy.  
Decision Tree performed poorly and overfitted.

---

##  5. Deep Learning Models & Results

| Deep Learning Model | Accuracy | Comments |
|---------------------|----------|----------|
| Simple RNN | ~70% | Weak for long sequences |
| LSTM | 93.72% | Good long-term memory |
| Bidirectional LSTM | 97.46% | Strong context learning |
| *GRU* | *97.78%* | ⭐ Best deep learning model |

Deep learning models performed very well, especially *GRU* and *Bidirectional LSTM*, which nearly matched ML accuracy.

---

##  6. Model Comparison Summary

###  Best Machine Learning Model  
*SGD Classifier – 98.49%*

###  Best Deep Learning Model  
*GRU – 97.78%*

###  Insight  
TF-IDF + linear models outperformed deep learning due to the dataset size.

