# Next Word Prediction Using RNN

This project trains an LSTM-based Recurrent Neural Network (RNN) to predict the next word in a sequence using text from Shakespeare's *Hamlet*.

## Project Overview

The workflow is implemented in `experiments.ipynb` and includes:

1. Loading text data from the NLTK Gutenberg corpus (`shakespeare-hamlet.txt`)
2. Preprocessing text and generating n-gram input sequences
3. Padding sequences and preparing features/labels
4. Training an LSTM model with TensorFlow/Keras
5. Saving trained artifacts for later inference

## Repository Structure

- `experiments.ipynb` — End-to-end notebook for data prep, training, and artifact export
- `requirements.txt` — Python dependencies
- `hamlet.tx` — Local copy of the Hamlet corpus text used in training
- `next_word_lstm.h5` — Saved trained LSTM model
- `tokenizer.pkl` — Saved tokenizer used to convert text to sequences

## Requirements

- Python 3.8+ (recommended)
- pip

Install dependencies:

```bash
pip install -r requirements.txt
```

## How to Run

1. Open the notebook:
   ```bash
   jupyter notebook experiments.ipynb
   ```
2. Run cells in order from top to bottom.
3. The notebook will:
   - download/load corpus data
   - train the next-word prediction model
   - save `next_word_lstm.h5` and `tokenizer.pkl`

## Notes

- Training configuration in the notebook currently uses:
  - Embedding + LSTM + Dropout + Dense output layer
  - Train/test split with `scikit-learn`
  - 50 training epochs
- You can modify model architecture and hyperparameters directly in `experiments.ipynb`.
