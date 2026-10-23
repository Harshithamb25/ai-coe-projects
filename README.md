# AI CoE — Machine Learning & Deep Learning Projects

A growing collection of hands-on **Machine Learning (ML) and Deep Learning (DL) workshop projects**, implemented in Python and documented to make the problem, workflow, evaluation, and key concepts easy to understand.

> **Repository status:** Project 1 is available. The remaining projects will be added as they are reviewed and documented.

## Project Collection

| # | Project | Main concepts | Status |
|---|---|---|---|
| 01 | [SMS Spam Classification — Multinomial Naive Bayes](projects/01-spam-classification/README.md) | Text preprocessing, bag-of-words, probabilistic classification, precision and recall | Available |
| 02 | Titanic Survival Prediction | Data cleaning, feature engineering, classification and evaluation | Planned |
| 03 | ANN Binary Classification with `make_moons` | TensorFlow / Keras | Available |
| 04 | CNN Dog–Cat Classification | Convolutional neural networks and image classification | Planned |
| 05 | Transformer-Based Next-Token Prediction | Self-attention and next-token prediction | Planned |

## Featured Project: SMS Spam Classification

A supervised text-classification baseline that predicts whether an SMS message is **spam** or **ham** (legitimate).

- **Dataset:** [SMS Spam Collection tutorial data](https://github.com/justmarkham/pycon-2016-tutorial)
- **Algorithm:** Multinomial Naive Bayes
- **Text representation:** Scikit-learn `CountVectorizer`
- **Evaluation:** Stratified 80/20 train/test split

### Test-set results

| Metric | Result |
|---|---:|
| Accuracy | 98.35% |
| Spam precision | 95.87% |
| Spam recall | 90.62% |
| Spam F1-score | 93.17% |
| ROC-AUC | 97.95% |

These results are from the notebook's current test evaluation. They describe performance on this dataset and split; they do not guarantee performance on newer or real-world messages.

**Explore the project:** [Project documentation](projects/01-spam-classification/README.md) · [Open notebook on GitHub](projects/01-spam-classification/spam_classifier_naive_bayes.ipynb) · [Open notebook in Google Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/01-spam-classification/spam_classifier_naive_bayes.ipynb)

## Tools & Libraries

The collection will use Python and project-appropriate libraries, including:

- Pandas and NumPy for data handling
- Matplotlib for visualisation
- Scikit-learn for classical ML, datasets, preprocessing, and evaluation
- TensorFlow/Keras or other suitable deep-learning tools where used in a project

The exact dependencies will be documented alongside each notebook as the collection grows.

## How to Use This Repository

1. Open a project's README to understand its objective, dataset, method, results, and limitations.
2. Open the corresponding Jupyter notebook on GitHub, or launch it in Google Colab using the link provided.
3. Run the notebook cells in order and follow any dataset setup instructions.
4. Treat reported metrics as specific to the documented data and evaluation procedure.

## Learning Goals

Across the collection, the projects aim to demonstrate:

- Data inspection, cleaning, and preprocessing
- Train/test splitting and leakage-aware evaluation
- Classification metrics and error analysis
- Classical machine learning and neural-network fundamentals
- Computer vision and transformer/self-attention basics
- Clear documentation, reproducible workflows, and honest reporting of limitations

## Scope

These are educational workshop projects intended to build and demonstrate foundational ML/DL skills. A strong result on a small or curated dataset is not, by itself, evidence of production readiness. Dataset sources, evaluation details, limitations, and any project-specific setup requirements should be checked in each project's documentation.

---

*This repository is being updated incrementally as each workshop notebook is reviewed and documented.*
