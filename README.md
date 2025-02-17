# Spam Detection NLP Assignment

## Overview
This repository contains an assignment completed in October 2020 for the Natural Language Processing (NLP) course in the Master of Data Science program at Universidad de San Andrés. The authors of the assignment are Paula Luvini, Florencia Ludueña, and Facundo Marconi. The objective was to explore different classifiers for spam detection based on email content, using a Kaggle competition dataset. The study focused on evaluating multiple models and selecting the best-performing one.

## Dataset
The dataset used for this assignment was the **Enron Corpus**, containing **4,000 emails**. An initial exploratory analysis revealed that the dataset was imbalanced, with only **23% of emails classified as spam**.

## Preprocessing Steps
1. **Text Cleaning**:
   - Removed punctuation and the word "Subject" (as it appeared in all emails).
   - Converted all text to lowercase.
   - Lemmatized words for normalization.
   
2. **Feature Engineering**:
   - Explored additional features such as email length and punctuation count.
   - Analyzed Parts of Speech (POS), observing differences in proper nouns and spacing between spam and ham emails.
   - Tested stemming but found that **lemmatization performed better**.
   
3. **TF-IDF Vectorization**:
   - Applied **Term Frequency-Inverse Document Frequency (TF-IDF)** to convert email text into a numerical matrix for classification.

## Model Selection
Supervised learning algorithms were tested for classification, including:
- **Support Vector Machines (SVM)**
- **K-Nearest Neighbors (KNN)**
- **Random Forest (RF)**
- **Logistic Regression**
- **Boosting Techniques**

To select the best model, **grid search and cross-validation with 5 folds** were performed. The final choice was **SVM with radial kernel (C=1)**, as it achieved the highest **accuracy (>80%)**.

## Conclusions
- Even with **basic text preprocessing**, the models achieved an accuracy consistently above 80%.
- Feature selection was **data-driven**, discarding those that did not contribute significantly to classification.
- The final approach was **conservative yet effective**, balancing available tools and dataset constraints.
- The study highlighted the importance of **proper preprocessing and feature engineering** in NLP classification tasks.

---
For more details, refer to the assignment report or code files in this repository.
