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

Training ran with early stopping (patience 15) and halted at epoch 25 of a
possible 50. The best checkpoint reached **99.19% validation accuracy** on
the 8,400-image holdout split.

The confusion matrix shows 88 misclassifications in total, spread thinly
across all ten digits — no single digit pair accounted for more than 8
errors. The most common confusion was a true **9 predicted as 4** (8 cases),
followed by 0→6, 7→1, and 8→6 (5 cases each). The classic 4/9 and 3/8
ambiguities are visible but small, which suggests the remaining errors are
mostly genuinely ambiguous handwriting rather than a systematic weakness.
<!-- Fill in your final validation accuracy and one sentence on what the
confusion matrix showed — e.g. which digit pairs were hardest. -->
