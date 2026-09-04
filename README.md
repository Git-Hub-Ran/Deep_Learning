# Digit Recognizer — CNN in PyTorch

A convolutional neural network that classifies handwritten digits from the
Kaggle [Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer/data)
dataset (MNIST in CSV form).

## What it does

- Loads the training and test CSVs and reshapes the flat pixel rows into
  28×28 single-channel images
- Trains a CNN with batch normalization and dropout for regularization
- Uses early stopping on validation loss to avoid overfitting
- Evaluates with a confusion matrix to see which digits get confused with
  which, rather than reporting accuracy alone

## Stack

- PyTorch
- NumPy / pandas
- Matplotlib and scikit-learn (confusion matrix)
- Google Colab

## Running it

Open the notebook in Google Colab and run the cells in order. The CSVs are
downloaded automatically from a public GitHub mirror of the Kaggle dataset,
so no Kaggle account or API token is required. A GPU runtime speeds up
training considerably.

## Results

<!-- Fill in your final validation accuracy and one sentence on what the
confusion matrix showed — e.g. which digit pairs were hardest. -->
