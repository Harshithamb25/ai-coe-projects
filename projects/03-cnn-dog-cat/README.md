# CNN Dog–Cat Classification

A binary image classifier built using TensorFlow/Keras and a CNN with exactly three convolutional layers.

## Concepts
- Image resizing and normalization
- Convolution and max pooling
- Dropout and early stopping
- Binary classification and evaluation metrics

## Dataset
Filtered Cats vs Dogs dataset: 3,000 images.
- Training: 1,600
- Validation: 400
- Held-out test: 1,000

## Model
Three convolutional layers with 32, 64, and 128 filters, followed by max pooling, dense layers, dropout, and sigmoid output.

## Test Results

| Metric | Score |
|---|---:|
| Accuracy | 70.50% |
| Precision | 68.81% |
| Recall | 75.00% |
| F1-score | 71.77% |
| ROC-AUC | 75.44% |

## Technologies
Python, TensorFlow/Keras, NumPy, Matplotlib, Scikit-learn.

## Notebook
`cnn_dog_cat_classification.ipynb`

The model was trained on CPU with early stopping. The results indicate room for improvement in generalization.
