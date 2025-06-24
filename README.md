# -SENTIMENT-ANALYSIS

COMPANY: CODTECH IT SOLUTIONS

NAME: PRISCILLA M

INTERN ID: CT04DN1650

DOMAIN: DATA ANALYSIS

DURATION: 4 WEEKS

MENTOR: NEELA SANTHOSH

* Sentiment Analysis on Mental Health Text (Kaggle)*

Sentiment analysis on a dataset of Reddit posts related to stress and anxiety. 

Using Natural Language Processing (NLP) techniques, built machine learning models to classify whether a user is stressed/anxious or not, based on their written post.

* Objective

To analyze emotionally nuanced text data and build a predictive model that can classify whether a post reflects signs of mental stress or anxiety.

* Dataset

- Source: Kaggle (Reddit Mental Health Dataset)
- Columns:
  - `Text`: Reddit post content
  - `is_stressed/anxious`: Target label (`1 = stressed/anxious`, `0 = not stressed`)

* Tools & Libraries Used

- Python (Jupyter Notebook)
- pandas, numpy – for data handling
- re, string – for text cleaning
- scikit-learn – for TF-IDF vectorization, model training & evaluation
- nltk – for natural language processing
- seaborn, matplotlib – for visualization

1. Data Cleaning
- Removed null values and duplicates from the Text column.
- Converted text to lowercase and removed punctuation, URLs, numbers, and extra spaces.

2. Feature Extraction
- Used **TF-IDF Vectorization** with unigrams and bigrams to convert cleaned text into numerical vectors.

3. Data Splitting
- Split the dataset into **Training (80%)** and **Testing (20%)** using stratified sampling to maintain class balance.

4. Model Training
- Trained two baseline models:
  - Logistic Regression
  - Multinomial Naive Bayes

5. Evaluation
- Evaluated models using:
  - Accuracy
  - Classification Report (Precision, Recall, F1-Score)
  - Confusion Matrix

* Model Results

1. Logistic Regression:
- Accuracy: **62.6%**
- Strength: Good recall for identifying stressed users
- Weakness: Struggled to classify non-stressed posts

2. Naive Bayes:
- Accuracy: **63.3%**
- Strength: High recall for stressed posts
- Weakness: Over-predicts stress; almost no recall for non-stressed posts

Key Insights

- Both models struggled to detect "not stressed" posts due to vocabulary skew.
  
- Logistic Regression with `class_weight='balanced'` and SMOTE oversampling can improve minority class recall.
  
- Further improvements could be achieved using models like SVM or BERT for better contextual understanding.

OUTPUT


