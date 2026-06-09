# Sentiment Analysis on Mental Health Statements

## Project Overview
This project performs sentiment analysis on real mental health statements sourced from social media platforms including Reddit, Twitter and Facebook. The goal is to classify text statements into one of seven mental health categories using Natural Language Processing (NLP) and Machine Learning techniques.

This project was completed as part of my Data Analytics internship at **CodeAlpha**.

---

## Dataset
- **Name:** Sentiment Analysis for Mental Health
- **Source:** [Kaggle — suchintikasarkar](https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health)
- **Size:** 52,681 statements after cleaning
- **Categories:** Normal, Depression, Suicidal, Anxiety, Bipolar, Stress, Personality Disorder

> The dataset is not uploaded to this repository due to its size (30MB). Please download it directly from the Kaggle link above.

---

## Tools & Libraries
- Python
- Pandas & NumPy
- NLTK (Natural Language Toolkit)
- Scikit-learn
- Matplotlib & Seaborn
- WordCloud

---

## Project Workflow
1. **Data Loading & Cleaning** — Removed missing values and irrelevant columns
2. **Text Preprocessing** — Lowercased text, removed URLs, punctuation, numbers and stopwords
3. **Exploratory Data Analysis** — Explored distribution of mental health categories
4. **Visualisation** — Generated word clouds and top 10 word frequency charts per category
5. **Modelling** — Built a Logistic Regression classifier using TF-IDF vectorization
6. **Evaluation** — Assessed model performance using classification report and confusion matrix

---

## Results
- **Overall Accuracy: 76%**
- The model performed best on **Normal** (F1: 0.89) and **Anxiety** (F1: 0.79)
- The model struggled most with **Stress** (F1: 0.58) and **Personality Disorder** (F1: 0.63) due to limited training data for those categories
- The most common confusion was between **Depression** and **Suicidal** statements, which is linguistically understandable as the two share very similar language patterns

---

## Visualisations
All charts are saved in the `/charts` folder:
- `1_status_distribution.png` — Distribution of mental health categories
- `2_wordclouds.png` — Word clouds per mental health status
- `3_top10_words.png` — Top 10 most frequent words per status
- `4_confusion_matrix.png` — Model confusion matrix

---

## Author
**Favour** — Data Analytics Intern at CodeAlpha
