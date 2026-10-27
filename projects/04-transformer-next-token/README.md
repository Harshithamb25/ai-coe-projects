# Transformer-Based Next-Token Prediction

A decoder-only Transformer language model implemented in PyTorch to explore **self-attention, positional embeddings, next-character prediction, and autoregressive text generation**.

This project demonstrates the core building blocks of Transformer-based language modelling through a small, self-contained educational experiment.

## Objectives

- Understand token embeddings and positional embeddings.
- Implement causal self-attention to prevent access to future tokens.
- Build a decoder-only Transformer using feedforward blocks and layer normalization.
- Train a model to predict the next character in a text sequence.
- Evaluate training and validation loss, and validation perplexity.
- Generate text autoregressively from a starting prompt.

## Technology Stack

- Python
- PyTorch
- NumPy
- Matplotlib
- Google Colab

## Model Architecture

The model processes character sequences and predicts the next character at each position.

1. **Character tokenisation:** Maps characters to integer IDs using a vocabulary derived from the training corpus.
2. **Token embeddings:** Converts character IDs into learned vector representations.
3. **Positional embeddings:** Adds sequence-position information to token representations.
4. **Causal self-attention:** Allows each position to attend only to itself and preceding positions.
5. **Feedforward blocks:** Transform the contextual representations.
6. **Layer normalisation and residual connections:** Support stable Transformer block computation.
7. **Language-model head:** Produces logits over the character vocabulary for next-character prediction.

The model is trained using cross-entropy loss and the AdamW optimiser. During generation, it repeatedly predicts and appends the next character to the sequence.

## Dataset and Preprocessing

The notebook uses a small, built-in text corpus, so a separate dataset download or API key is not required.

- Text is converted to lowercase.
- A character-level vocabulary is constructed from the corpus.
- Text is encoded into integer token IDs.
- The data is divided into training and validation portions.
- Fixed-length context windows are used to create next-character prediction examples.

**Important:** This is character-level language modelling, not word-level tokenisation or a large-scale pretrained language model.

## Training Configuration

| Parameter | Configuration |
|---|---|
| Model type | Decoder-only Transformer |
| Prediction task | Next-character prediction |
| Context length | 64 characters |
| Batch size | 32 |
| Training iterations | 800 |
| Optimiser | AdamW |
| Learning rate | 0.0003 |
| Loss function | Cross-entropy |
| Evaluation | Training and validation loss |

## Evaluation Results

The notebook was executed successfully in Google Colab.

| Evaluation metric | Result |
|---|---:|
| Final training loss | 0.0910 |
| Final validation loss | 0.0917 |
| Validation perplexity | 1.10 |

The training and validation losses are close in this run, indicating similar measured loss on the two splits. The notebook also plots loss curves, inspects next-character probabilities, and demonstrates autoregressive generation.

A low validation perplexity is encouraging within this experiment, but it should not be interpreted as evidence of broad language understanding. The small corpus and character-level prediction task strongly limit what these numbers tell us about generalisation.

## How to Run

1. Open the notebook using the Google Colab link below.
2. Select **Runtime → Run all**.
3. Allow the model to train and evaluation cells to finish.
4. Inspect the training and validation loss plot.
5. Review validation perplexity and the next-character probability output.
6. Experiment with the text-generation prompt and observe the generated output.

No external dataset or API key is required.

## Project Files

- `transformer_next_token_prediction.ipynb` — complete implementation, training, evaluation, visualisation, and generation.
- `README.md` — project overview, methodology, results, and limitations.

## Limitations

- The corpus is small and does not represent the diversity of natural language.
- The model predicts characters rather than word or subword tokens.
- Generated text may be repetitive, incoherent, or overly dependent on patterns in the training corpus.
- Validation loss and perplexity are specific to this corpus, vocabulary, and tokenisation approach.
- This experiment is intended for learning and experimentation, not production deployment.

## Future Improvements

- Train on a larger, appropriately licensed text corpus.
- Compare character-level and subword tokenisation.
- Experiment with model depth, embedding dimensions, and attention heads.
- Add generation controls such as temperature and top-k sampling.
- Compare performance across different corpus sizes and training configurations.

## Notebook

[**Open the Transformer Next-Token Prediction notebook in Google Colab**](https://colab.research.google.com/github/Harshithamb25/ai-coe-projects/blob/main/projects/04-transformer-next-token/transformer_next_token_prediction.ipynb)

---

*Project status: Complete — notebook execution and evaluation completed.*
