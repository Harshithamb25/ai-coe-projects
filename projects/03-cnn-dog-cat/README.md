# CNN — Dog–Cat Image Classification

## Overview

A binary image-classification baseline built with TensorFlow/Keras. The CNN uses three convolutional layers to distinguish cats from dogs and uses dropout and early stopping during training.

## Dataset

- **Source:** [Filtered Cats vs Dogs dataset](https://download.mlcc.google.com/mledu-datasets/cats_and_dogs_filtered.zip)
- **Training-source directory:** 2,000 images (1,000 cats and 1,000 dogs)
- **Training split:** 1,600 images
- **Validation split:** 400 images
- **Held-out test set:** 1,000 images (500 cats and 500 dogs), from the separate validation directory in the downloaded dataset

The training-source directory is split 80/20 for training and validation. The separate 1,000-image set is used for final evaluation.

## Model Architecture

- **Input:** 128 × 128 RGB images, rescaled to [0, 1]
- **Convolutional layers:** 32, 64, and 128 filters, each followed by max pooling
- **Classifier head:** Flatten, Dense(128, ReLU), Dropout(0.4), Dense(1, sigmoid)
- **Optimizer:** Adam, learning rate 0.001
- **Loss:** Binary cross-entropy
- **Training control:** Early stopping on validation loss (patience 3, restore best weights)
- **Maximum epochs:** 12
- **Training environment:** CPU

## Held-out Test Results

| Metric | Score |
|---|---:|
| Accuracy | 70.50% |
| Precision | 68.81% |
| Recall | 75.00% |
| F1-score | 71.77% |
| ROC-AUC | 75.44% |

Per-class test results:

| Class | Precision | Recall | F1-score | Support |
|---|---:|---:|---:|---:|
| Cats | 73% | 66% | 69% | 500 |
| Dogs | 69% | 75% | 72% | 500 |

These results are a baseline, with clear scope for improvement. The notebook reports the metrics from the held-out set; they should not be interpreted as production performance.

## Run the Notebook

- [View notebook on GitHub](cnn_dog_cat_classification.ipynb)
- [Open notebook in Google Colab](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/03-cnn-dog-cat/cnn_dog_cat_classification.ipynb)

Run the notebook cells in order. The notebook downloads and prepares the dataset as part of the workflow.

## Concepts Demonstrated

- Image resizing and normalization
- Convolution and max pooling
- Binary classification with a sigmoid output
- Dropout and early stopping
- Precision, recall, F1-score, ROC-AUC, and per-class evaluation

## Limitations and Next Steps

- Performance is moderate and may be affected by the small image size and simple architecture.
- Inspect misclassified images and training/validation curves before changing the model.
- Potential next steps include data augmentation, transfer learning, and systematic hyperparameter experiments.

## Conclusion

This project demonstrates an end-to-end CNN workflow and documents a **70.50% held-out test accuracy** baseline honestly, including its limitations.
