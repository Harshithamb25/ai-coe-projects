# Artificial Neural Network for Binary Classification — Make Moons

## Overview

This project implements a feedforward Artificial Neural Network (ANN) to classify two interleaving moon-shaped classes using Scikit-learn's `make_moons` dataset. The experiment demonstrates how nonlinear activation functions enable a neural network to learn a curved decision boundary.

## Objectives

- Generate and explore a synthetic binary classification dataset.
- Apply a stratified train-test split and feature standardization.
- Build and train an ANN using TensorFlow/Keras.
- Evaluate classification performance using multiple metrics.
- Visualize training curves, the confusion matrix, and the learned decision boundary.

## Tech Stack

- Python
- NumPy and Pandas
- Matplotlib
- Scikit-learn
- TensorFlow / Keras

## Dataset

The dataset contains 1,500 generated samples, two numerical input features, and two classes. Gaussian noise is introduced using `noise=0.20`.

| Setting | Value |
|---|---|
| Samples | 1,500 |
| Input features | 2 |
| Classes | 2 |
| Training samples | 1,200 |
| Testing samples | 300 |
| Random state | 42 |

## Model Architecture

| Layer | Configuration |
|---|---|
| Input | 2 features |
| Hidden layer 1 | 16 neurons, ReLU |
| Hidden layer 2 | 8 neurons, ReLU |
| Output | 1 neuron, Sigmoid |

**Total trainable parameters:** 193

### Training Configuration

- Optimizer: Adam
- Learning rate: 0.001
- Loss function: Binary cross-entropy
- Epochs: 100
- Batch size: 32
- Validation split: 20% of the training data
- Classification threshold: 0.5

Feature scaling is fitted only on the training subset and then applied to the test subset to avoid test-data leakage.

## Test Results

The following results were obtained in this experiment:

| Metric | Result |
|---|---:|
| Accuracy | 96.00% |
| Precision | 0.9600 |
| Recall | 0.9600 |
| F1-score | 0.9600 |
| ROC-AUC | 0.9940 |

The model achieved strong classification performance on the held-out test set. The ROC-AUC indicates excellent discrimination between the classes across probability thresholds.

## Key Visualizations

The notebook includes:
- Class distribution of the generated dataset
- Training and validation loss curves
- Training and validation accuracy curves
- Confusion matrix
- ANN decision-boundary visualization

The decision-boundary plot demonstrates that the network learns a nonlinear separation that follows the curved structure of the two classes.

## How to Run

1. Open the notebook in Google Colab.
2. Run the cells sequentially from top to bottom.
3. Review the training curves, evaluation metrics, and decision-boundary plot.

All required libraries are commonly available in Google Colab.

## Limitations

- The dataset is synthetic and does not represent every real-world classification problem.
- Performance depends on the selected architecture, hyperparameters, and random initialization.
- The experiment does not establish that this ANN outperforms every alternative classifier.
- Results on this dataset do not guarantee similar performance on unseen real-world datasets.

## Future Improvements

- Compare the ANN against Logistic Regression, Decision Trees, and Support Vector Machines.
- Experiment with different architectures and activation functions.
- Evaluate performance across multiple random seeds.
- Explore early stopping and regularization.

## Conclusion

This project demonstrates the use of a feedforward ANN for nonlinear binary classification. With two ReLU hidden layers and a sigmoid output, the model achieved 96.00% test accuracy and 0.9940 ROC-AUC on the generated make-moons dataset.

The experiment provides practical experience with neural network design, training, evaluation, and decision-boundary visualization.
