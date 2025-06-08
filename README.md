# News Article Classification

## Overview

In the age of digital information, news content is constantly generated and shared across platforms. Automatically classifying this content into categories like **sports**, **politics**, or **technology** is essential for efficient content management, recommendation systems, and enhancing user experience.

This project aims to build a machine learning model that classifies news articles based on their textual content using natural language processing and classification algorithms.

## Problem Statement

The primary goal is to develop a robust and scalable machine learning model that can:

* Automatically categorize news articles into predefined categories.
* Preprocess and vectorize the text data for model input.
* Evaluate and optimize multiple classification models for accuracy and performance.
* Extract insights from the model to understand which features are most informative.

## Dataset Description

* **Source**: `data_news.csv`
* **Features Used**: `headline`, `short_description` (combined into a single text field)
* **Target Variable**: `category`
* **Number of Categories**: 10 (e.g., Sports, Politics, Entertainment, Technology, etc.)

## Methodology

### 1. Data Preprocessing

* Combined `headline` and `short_description` into one text column.
* Applied standard text cleaning procedures:

  * Converted text to lowercase.
  * Removed punctuation and digits.
  * Removed stopwords.
  * Performed lemmatization.

### 2. Feature Extraction

* Used **TF-IDF Vectorization** with the following settings:

  * Maximum 5000 features
  * Included unigrams and bigrams
* Performed **Exploratory Data Analysis (EDA)** to understand category distribution and term frequencies.

### 3. Model Development

Implemented and compared the following models:

* **Logistic Regression**
* **Multinomial Naive Bayes**
* **Support Vector Machine (SVM)**

The dataset was split into:

* **80% training data**
* **20% testing data**

Hyperparameter tuning and cross-validation were used where applicable.

### 4. Evaluation

* Models were evaluated using accuracy, precision, recall, and F1-score.
* The best-performing model was selected based on macro-averaged F1-score and classification accuracy.
* Classification report and confusion matrix were used to assess performance across all categories.

## Deliverables

* Jupyter Notebook containing:

  * Data preprocessing steps
  * Feature extraction
  * Model training and evaluation
* Final classification report and visualizations
* Short video (under 5 minutes) presenting the methodology, insights, and model performance

## Success Criteria

* High performance in classification metrics on unseen data
* Generalization ability across various categories
* Well-documented methodology and reproducible results

## Tools and Libraries

* Python
* pandas, numpy
* scikit-learn
* nltk, spacy
* matplotlib, seaborn
* Jupyter Notebook

## Conclusion

This project demonstrates how machine learning and NLP techniques can be applied to automate the classification of news articles. The final model successfully categorizes articles into multiple categories, providing a foundation for real-world applications in news aggregation and content recommendation systems.

