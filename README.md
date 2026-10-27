# AI CoE — Machine Learning & Deep Learning Projects

A focused portfolio of hands-on **machine learning, deep learning, and language modelling experiments** built through workshop learning and independent practice. Each completed project includes a notebook, documented methodology, evaluation results, and limitations.

## Project Collection

| # | Project | Techniques | Status |
|---|---|---|---|
| 01 | [SMS Spam Classification](projects/01-spam-classification/README.md) | Text preprocessing, bag-of-words, Multinomial Naive Bayes | Complete |
| 02 | [ANN — Make Moons Classification](projects/02-ann-make-moons/README.md) | Feedforward neural networks, nonlinear decision boundaries | Complete |
| 03 | [CNN — Dog–Cat Classification](projects/03-cnn-dog-cat/README.md) | Convolution, pooling, dropout, image classification | Complete |
| 04 | [Transformer-Based Next-Token Prediction](projects/04-transformer-next-token/README.md) | Causal self-attention, positional embeddings, autoregressive generation | Complete |
| 05 | Titanic Survival Prediction | Data preparation, feature engineering, classification | Planned |

## Featured Projects

### 01 · SMS Spam Classification — Multinomial Naive Bayes

Classifies SMS messages as **spam** or **ham** using bag-of-words features and a probabilistic classifier.

- **Data:** 5,158 records after duplicate cleaning
- **Features:** Scikit-learn `CountVectorizer`
- **Evaluation:** Stratified train/test split

| Held-out test metric | Score |
|---|---:|
| Accuracy | 98.35% |
| Spam precision | 95.87% |
| Spam recall | 90.62% |
| Spam F1-score | 93.17% |
| ROC-AUC | 97.95% |

Links: [Project details](projects/01-spam-classification/README.md) · [Notebook](projects/01-spam-classification/spam_classifier_naive_bayes.ipynb) · [Open in Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/01-spam-classification/spam_classifier_naive_bayes.ipynb) · [Dataset source](https://github.com/justmarkham/pycon-2016-tutorial)

### 02 · Artificial Neural Network — Make Moons

A feedforward ANN learns a nonlinear decision boundary for two interleaving classes generated with Scikit-learn's `make_moons`.

- **Data:** 1,500 synthetic samples; 1,200 train / 300 test
- **Architecture:** Dense layers with 16 and 8 ReLU units, followed by a sigmoid output
- **Training:** Adam, binary cross-entropy; scaling fitted on training data only

| Held-out test metric | Score |
|---|---:|
| Accuracy | 96.00% |
| Precision | 96.00% |
| Recall | 96.00% |
| F1-score | 96.00% |
| ROC-AUC | 99.40% |

Links: [Project details](projects/02-ann-make-moons/README.md) · [Notebook](projects/02-ann-make-moons/ann_make_moons_classification.ipynb) · [Open in Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/02-ann-make-moons/ann_make_moons_classification.ipynb)

### 03 · CNN — Dog–Cat Image Classification

A three-convolution-layer CNN classifies cat and dog images using TensorFlow/Keras. Early stopping is used to limit overfitting during training.

- **Data:** 2,000 training-source images (1,600 training / 400 validation) and a separate 1,000-image held-out test set
- **Architecture:** Conv2D layers with 32, 64, and 128 filters; max pooling; dense layer; dropout; sigmoid output
- **Input:** 128 × 128 RGB images

| Held-out test metric | Score |
|---|---:|
| Accuracy | 70.50% |
| Precision | 68.81% |
| Recall | 75.00% |
| F1-score | 71.77% |
| ROC-AUC | 75.44% |

The baseline leaves room for improvement; results are reported as measured rather than presented as production-level performance.

Links: [Project details](projects/03-cnn-dog-cat/README.md) · [Notebook](projects/03-cnn-dog-cat/cnn_dog_cat_classification.ipynb) · [Open in Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/03-cnn-dog-cat/cnn_dog_cat_classification.ipynb) · [Dataset source](https://download.mlcc.google.com/mledu-datasets/cats_and_dogs_filtered.zip)

### 04 · Transformer-Based Next-Token Prediction

An educational, decoder-only Transformer implemented in PyTorch to explore causal self-attention, positional embeddings, next-character prediction, and autoregressive text generation.

- **Data:** A small, built-in text corpus
- **Architecture:** Token embeddings, positional embeddings, causal self-attention, feedforward blocks, layer normalization, and a language-model output head
- **Training:** Next-character prediction using cross-entropy loss and AdamW
- **Generation:** Autoregressive text generation based on a starting prompt
- **Evaluation:** Training loss, validation loss, and validation perplexity

| Evaluation metric | Result |
|---|---:|
| Final training loss | 0.0910 |
| Final validation loss | 0.0917 |
| Validation perplexity | 1.10 |

The notebook was executed successfully in Google Colab. The training and validation losses are close in this run. However, the small corpus limits generalisation, and the low perplexity should not be interpreted as evidence of general-purpose language understanding or production-level text generation.

Links: [Project details](projects/04-transformer-next-token/README.md) · [Notebook](projects/04-transformer-next-token/transformer_next_token_prediction.ipynb) · [Open in Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/04-transformer-next-token/transformer_next_token_prediction.ipynb)

## Tools and Libraries

- **Python** — implementation
- **Pandas and NumPy** — data preparation and numerical computing
- **Matplotlib** — visualisation
- **Scikit-learn** — preprocessing, datasets, classical ML, and evaluation
- **TensorFlow / Keras** — neural-network models and training
- **PyTorch** — Transformer implementation, self-attention, and language modelling

Each notebook lists or imports the libraries needed for its experiment. The notebooks are designed to be run sequentially in Google Colab; dataset and setup requirements are documented in the relevant project README.

## Suggested Workflow

1. Choose a project from the table above.
2. Read its README for the dataset, method, results, and limitations.
3. Open the notebook on GitHub or launch it in Google Colab.
4. Run cells in order and inspect the plots, metrics, generated outputs, and error analysis.

## Learning Focus

- Data cleaning, feature extraction, and preprocessing
- Stratified evaluation and avoiding test-data leakage
- Classification metrics, confusion matrices, and error analysis
- Probabilistic models and feedforward neural networks
- Nonlinear decision boundaries and computer vision
- Transformer architecture, causal self-attention, and positional embeddings
- Next-token prediction and autoregressive generation
- Clear experiment documentation and reproducible workflows

## Scope and Limitations

This is an educational project collection, not a production ML system. The spam project uses a curated dataset, the ANN project uses synthetic data, the CNN project uses a filtered image dataset, and the Transformer project uses a small built-in text corpus. Results describe these experiments only and do not guarantee performance on real-world data. Transformer outputs are limited by the training corpus and model scale.

The Titanic Survival Prediction project remains **planned** until its implementation and documentation are complete.

---

*Projects are added incrementally as experiments are completed and documented.*
