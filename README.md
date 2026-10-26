# AI CoE — Machine Learning & Deep Learning Projects

A curated collection of hands-on **Machine Learning (ML) and Deep Learning (DL) projects** developed through workshop learning and experimentation. Each project includes implementation notebooks, evaluation results, explanations of key concepts, and documented limitations.

## Project Collection

| # | Project | Main Concepts | Status |
|---|---|---|---|
| 01 | [SMS Spam Classification — Multinomial Naive Bayes](projects/01-spam-classification/README.md) | Text preprocessing, bag-of-words, probabilistic classification, precision and recall | Available |
| 02 | [ANN Binary Classification with `make_moons`](https://github.com/Harshithamb25/ai-coe-projects/tree/main/projects/02-ann-make-moons) | Neural networks, ReLU and sigmoid activations, nonlinear decision boundaries | Available |
| 03 | CNN Dog–Cat Classification | Convolutional neural networks and image classification | Planned |
| 04 | Transformer-Based Next-Token Prediction | Self-attention and next-token prediction | Planned |
| 05 | Titanic Survival Prediction | Data cleaning, feature engineering, classification and evaluation | Planned |

## Featured Projects

### 01. SMS Spam Classification

A supervised text-classification model that predicts whether an SMS message is **spam** or **ham** (legitimate).

- **Dataset:** [SMS Spam Collection tutorial data](https://github.com/justmarkham/pycon-2016-tutorial)
- **Algorithm:** Multinomial Naive Bayes
- **Text representation:** Scikit-learn `CountVectorizer`
- **Evaluation:** Stratified 80/20 train-test split

**Test-set results**

| Metric | Result |
|---|---:|
| Accuracy | 98.35% |
| Spam precision | 95.87% |
| Spam recall | 90.62% |
| Spam F1-score | 93.17% |
| ROC-AUC | 97.95% |

Explore: [Project README](projects/01-spam-classification/README.md) · [Jupyter Notebook](projects/01-spam-classification/spam_classifier_naive_bayes.ipynb) · [Open in Google Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/01-spam-classification/spam_classifier_naive_bayes.ipynb)

### 02. Artificial Neural Network — Make Moons Classification

A feedforward Artificial Neural Network built to classify two interleaving moon-shaped classes. This project demonstrates how nonlinear activation functions enable a neural network to learn a curved decision boundary.

- **Dataset:** Scikit-learn `make_moons`, with 1,500 generated samples
- **Architecture:** Two hidden layers with 16 and 8 neurons, followed by a sigmoid output layer
- **Framework:** TensorFlow / Keras
- **Training:** Adam optimizer with binary cross-entropy loss
- **Evaluation:** Accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrix

**Test-set results**

| Metric | Result |
|---|---:|
| Accuracy | 96.00% |
| Precision | 96.00% |
| Recall | 96.00% |
| F1-score | 96.00% |
| ROC-AUC | 99.40% |

Explore: [Project README](projects/02-ann-make-moons/README.md) · [Jupyter Notebook](projects/02-ann-make-moons/ann_make_moons_classification.ipynb) · [Open in Google Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/02-ann-make-moons/ann_make_moons_classification.ipynb)


## Tools & Libraries

The collection uses Python and project-appropriate libraries, including:

- **NumPy and Pandas** — numerical computing and data handling
- **Matplotlib** — data and model visualization
- **Scikit-learn** — datasets, preprocessing, classical ML algorithms, and evaluation
- **TensorFlow / Keras** — neural-network construction and training

Dependencies and setup instructions are documented alongside individual projects where needed.

## How to Use This Repository

1. Browse the project collection and select a topic.
2. Read its README to understand the objective, dataset, methodology, results, and limitations.
3. Open the corresponding Jupyter notebook on GitHub or launch it in Google Colab.
4. Run the notebook cells in order and follow any project-specific setup instructions.
5. Review the evaluation metrics and visualizations to understand the model's performance.

## Learning Goals

These projects explore:

- Data inspection, cleaning, and preprocessing
- Train-test splitting and leakage-aware evaluation
- Classification metrics and error analysis
- Probabilistic machine learning and neural-network fundamentals
- Nonlinear decision boundaries and model visualization
- Computer vision and transformer/self-attention concepts
- Reproducible experiments and clear technical documentation

## Scope and Limitations

This repository is an educational collection of workshop projects intended to demonstrate foundational ML and DL concepts. Results from synthetic or curated datasets do not, by themselves, establish production readiness or guarantee performance on real-world data.

Each project's documentation should be consulted for its dataset source, evaluation procedure, limitations, and setup requirements.

---

*Projects are added incrementally as their implementations are completed.*
