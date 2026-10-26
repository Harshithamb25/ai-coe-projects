# Artificial Neural Network — Make Moons Classification

## Overview

A feedforward Artificial Neural Network (ANN) classifies two interleaving moon-shaped classes generated with Scikit-learn's `make_moons`. The experiment demonstrates how nonlinear activations help a network learn a curved decision boundary.

## Dataset

| Setting | Value |
|---|---:|
| Generated samples | 1,500 |
| Input features | 2 |
| Classes | 2 |
| Training samples | 1,200 |
| Test samples | 300 |
| Noise | 0.20 |
| Random state | 42 |

The data is split into training and test subsets. Feature standardization is fitted on the training subset only, then applied to the test subset to avoid test-data leakage.

## Model Architecture

| Layer | Configuration |
|---|---|
| Input | 2 features |
| Hidden layer 1 | 16 neurons, ReLU |
| Hidden layer 2 | 8 neurons, ReLU |
| Output | 1 neuron, sigmoid |

**Trainable parameters:** 193

## Training Configuration

- Framework: TensorFlow / Keras
- Optimizer: Adam, learning rate 0.001
- Loss: Binary cross-entropy
- Epochs: 100
- Batch size: 32
- Validation split: 20% of the training data
- Classification threshold: 0.5

## Held-out Test Results

| Metric | Score |
|---|---:|
| Accuracy | 96.00% |
| Precision | 96.00% |
| Recall | 96.00% |
| F1-score | 96.00% |
| ROC-AUC | 99.40% |

These scores describe this experiment on a synthetic dataset; they do not establish that the ANN is better than every alternative classifier.

## Visualizations

The notebook includes the generated class distribution, training/validation loss and accuracy curves, confusion matrix, and learned decision boundary.

## Run the Notebook

- [View notebook on GitHub](ann_make_moons_classification.ipynb)
- [Open notebook in Google Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/02-ann-make-moons/ann_make_moons_classification.ipynb)

Run cells sequentially. The common scientific Python and TensorFlow/Keras libraries are available in Google Colab.

## Limitations and Next Steps

- The dataset is synthetic and has only two input features.
- Performance can vary with initialization, architecture, and hyperparameters.
- Compare with Logistic Regression, Decision Trees, and Support Vector Machines.
- Repeat experiments across multiple random seeds and test regularization or early stopping.

## Conclusion

With two ReLU hidden layers and a sigmoid output, the network achieved **96.00% test accuracy** and **99.40% ROC-AUC** in this make-moons experiment.
