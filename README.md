# Formative-Assessment-NLP---Emotion-Classification-in-Text


# Dataset:
https://drive.google.com/file/d/1HWczIICsMpaL8EJyu48ZvRFcXx3_pcnb/view?usp=drive_link


# 1. Loading and Preprocessing 

## a) Load the Dataset

First, we'll load the dataset into a pandas DataFrame. Since the data is in a text format, we'll assume it's either a .csv or .txt file, and we can use pandas.read_csv() or an appropriate function to load it.

## b) Preprocessing Steps:

Text Cleaning:

Convert text to lowercase.
Remove punctuations, numbers, and special characters.
Strip unnecessary white spaces.
Impact: Cleaning helps the model focus on meaningful words and reduces noise.
Tokenization:

Split the text into words (tokens).
We can use the nltk or spaCy library for tokenization.
Impact: Tokenizing the text allows us to analyze and manipulate individual words, which is essential for text classification.
Stopword Removal:

Remove common words like "the," "and," and "is" that do not contribute much to understanding the sentiment/emotion.
We can use nltk.corpus.stopwords or a custom stopword list.
Impact: Reducing stopwords can improve model performance by removing words that add noise.


# 2. Feature Extraction 

## a) CountVectorizer or TfidfVectorizer

We need to convert the text data into numerical form for the machine learning model. Two common methods are:

CountVectorizer: Converts a collection of text documents to a matrix of token counts (bag of words). This model counts the occurrences of words and represents the text as a vector.
TfidfVectorizer: Instead of raw counts, it calculates the Term Frequency-Inverse Document Frequency (TF-IDF), which adjusts word counts based on how frequently they appear across the dataset.

# 3. Model Development 

## a) Naive Bayes
Naive Bayes is a probabilistic classifier that works well for text classification because of its simplicity and effectiveness in high-dimensional spaces like text data.

## b) Support Vector Machine (SVM)

SVM is a powerful classifier that tries to find a hyperplane to separate classes. It can handle high-dimensional spaces well and is known for good performance on text classification.

# 4. Model Comparison 

To evaluate and compare the models, we can use common metrics such as accuracy, precision, recall, and F1-score.


Explanation:
Naive Bayes is suitable for text classification because it assumes independence between features (words), which works well with bag-of-words and TF-IDF representations.
SVM performs well with high-dimensional data and can be more robust than Naive Bayes, especially for complex datasets. It finds the optimal boundary for class separation.
