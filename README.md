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

## Key Insights

### 1. Depression is alarmingly prevalent
Out of 52,681 statements, Depression (15,404) and Suicidal (10,652) together account for over 49% of the entire dataset. Combined with Anxiety, Bipolar, Stress and Personality Disorder, only 31% of statements were classified as Normal. This suggests that among people who openly express their mental state online, distress is far more common than wellbeing.

### 2. Work and stress are deeply connected
In the Stress category, the word "work" was the single most dominant term after common words were removed. This points strongly to workplace pressure as a leading driver of stress, which has significant implications for employee wellbeing programs and organizational mental health policies.

### 3. Suicidal language is closely tied to depression
The model's biggest confusion was between Depression and Suicidal statements — 555 Suicidal statements were misclassified as Depression and 595 Depression statements were misclassified as Suicidal. This linguistic overlap suggests that suicidal ideation often develops from and sounds very similar to depressive language, reinforcing the importance of taking all expressions of depression seriously.

### 4. People with Bipolar disorder use more clinical language
Unlike other categories where people described feelings and experiences, the Bipolar word cloud prominently featured words like "medication", "doctor" and "med". This suggests people discussing Bipolar disorder are more likely to be engaged with the healthcare system and discussing treatment rather than just expressing raw emotion.

### 5. Loneliness is a recurring theme across categories
Words like "alone", "people", "friend" and "family" appeared consistently across Depression, Suicidal and Personality Disorder categories. This suggests that relationship difficulties and feelings of isolation are a common thread running through multiple mental health conditions.

### 6. First person language dominates all categories
The word "im" (I'm) was the most frequent word across nearly every mental health category. This confirms that these are deeply personal, first person expressions of lived experience — not observations or general statements — making this dataset a uniquely honest window into how people actually feel.

---

## Recommendations

1. **Mental health platforms should prioritize Depression and Suicidal content moderation** — given how prevalent and intertwined these two categories are, automated detection tools should be trained to treat them as a connected risk spectrum rather than separate categories

2. **Workplace wellness programs need urgent attention** — the dominance of "work" in stress-related statements suggests organizations should invest more heavily in employee mental health support

3. **More data is needed for underrepresented categories** — Personality Disorder had only 1,077 statements, leading to weaker model performance. Future datasets should deliberately oversample underrepresented conditions for more balanced and reliable classification

4. **Social connection interventions could address multiple conditions simultaneously** — since loneliness appears across Depression, Suicidal and Personality Disorder categories, community building and social support programs could have broad mental health benefits

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
