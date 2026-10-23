# SMS Spam Classification Using Multinomial Naive Bayes

## Overview

This project implements a supervised machine learning model to classify SMS messages as **spam** or **ham** (legitimate messages) using the Multinomial Naive Bayes algorithm.

The project demonstrates text preprocessing, bag-of-words feature extraction, model training, and evaluation using multiple classification metrics.

## Dataset

- **Source:** [SMS Spam Collection](https://github.com/justmarkham/pycon-2016-tutorial)
- **Original records:** 5,572 messages
- **Records after cleaning:** 5,158 messages
- **Ham messages:** 4,516
- **Spam messages:** 642

Exact duplicate label-message pairs are removed during cleaning.

## Technologies

- Python
- Pandas and NumPy
- Scikit-learn
- CountVectorizer
- Multinomial Naive Bayes
- Matplotlib

## Workflow

1. Load and inspect the SMS dataset.
2. Clean the messages and remove duplicate records.
3. Separate text features and target labels.
4. Split the data into training and testing sets using stratified sampling.
5. Convert text into numerical bag-of-words features.
6. Train the Multinomial Naive Bayes classifier.
7. Evaluate predictions using classification metrics and a confusion matrix.
8. Test the classifier with sample messages.

## Results

| Metric | Test result |
|---|---:|
| Accuracy | 98.35% |
| Spam precision | 95.87% |
| Spam recall | 90.62% |
| Spam F1-score | 93.17% |
| ROC-AUC | 97.95% |

The model correctly classified most messages in the test set. It produced 5 false positives and 12 false negatives.

## How to Run

1. Open the notebook in Google Colab.
2. Run the cells from top to bottom.
3. Review the evaluation metrics, confusion matrix, and sample predictions.

## Key Learning Outcomes

- Supervised text classification
- Bag-of-words feature extraction
- Bayes theorem and conditional independence
- Laplace smoothing
- Train/test splitting and stratification
- Precision, recall, F1-score, and ROC-AUC
- Interpreting false positives and false negatives

## Limitations

- Bag-of-words features do not understand word order or contextual meaning.
- The dataset has an imbalanced class distribution.
- Spam language can change over time.
- Performance on this test set does not guarantee real-world performance.

This project is an educational machine learning baseline and is not a production-ready spam filtering system.
