# SMS Spam Classification — Multinomial Naive Bayes

## Overview

A supervised text-classification baseline that labels SMS messages as **spam** or **ham** (legitimate messages). The workflow covers data cleaning, bag-of-words feature extraction, model training, and held-out evaluation.

## Dataset

- **Source:** [SMS Spam Collection tutorial data](https://github.com/justmarkham/pycon-2016-tutorial)
- **Original records:** 5,572 messages
- **Records after cleaning:** 5,158 messages
- **Ham:** 4,516
- **Spam:** 642
- **Cleaning:** Exact duplicate label-message pairs are removed.

## Method

1. Load and inspect the dataset.
2. Remove duplicate records and separate text from labels.
3. Split the data using stratified sampling.
4. Convert message text to bag-of-words features with Scikit-learn `CountVectorizer`.
5. Train a Multinomial Naive Bayes classifier.
6. Evaluate predictions and inspect the confusion matrix and sample messages.

## Held-out Test Results

| Metric | Score |
|---|---:|
| Accuracy | 98.35% |
| Spam precision | 95.87% |
| Spam recall | 90.62% |
| Spam F1-score | 93.17% |
| ROC-AUC | 97.95% |

The test confusion matrix contains **5 false positives** and **12 false negatives**. Precision and recall are reported for the spam class.

## Run the Notebook

- [View notebook on GitHub](spam_classifier_naive_bayes.ipynb)
- [Open notebook in Google Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/01-spam-classification/spam_classifier_naive_bayes.ipynb)

Run cells from top to bottom and review the metrics, confusion matrix, and sample predictions.

## Key Concepts

- Supervised text classification
- Bag-of-words and feature extraction
- Multinomial Naive Bayes and Laplace smoothing
- Stratified train/test splitting
- Precision, recall, F1-score, ROC-AUC, and error analysis

## Limitations

- Bag-of-words does not represent word order or contextual meaning.
- The dataset has more ham messages than spam messages.
- Spam vocabulary can change over time.
- Results on this curated test set do not guarantee real-world performance.

This project is an educational baseline, not a production-ready spam filter.
