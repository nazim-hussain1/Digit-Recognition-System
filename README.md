# Digit Recognition System

A Convolutional Neural Network (CNN) that classifies handwritten digits (0–9), trained on the MNIST dataset using TensorFlow/Keras. Includes a custom preprocessing pipeline to run predictions on your own uploaded digit images, not just the MNIST test set.

## Overview

This project loads and preprocesses the MNIST dataset, trains a CNN classifier, and then applies the trained model to custom handwritten digit images — with a contrast-enhancement step to improve accuracy on real-world photos, which tend to be noisier and less centered than MNIST's clean training data.

## Model Architecture


- **Optimizer:** Adam
- **Loss:** Categorical Crossentropy
- **Epochs:** 10
- **Batch size:** 32

## Tech Stack

- Python
- TensorFlow / Keras
- NumPy
- PIL (Pillow)
- Matplotlib
- Google Colab

## How It Works

1. Loads and normalizes the MNIST dataset (pixel values scaled to [0, 1])
2. Reshapes data to `(28, 28, 1)` and one-hot encodes labels
3. Trains the CNN for 10 epochs
4. Saves the trained model as `digit_recognition_model.h5`
5. Preprocesses a custom uploaded image: converts to grayscale, resizes to 28x28, enhances contrast
6. Runs the trained model on the processed image and outputs the predicted digit

## Running It

Open the notebook in Google Colab (badge below), run all cells in order, and upload your own digit image when prompted to see a live prediction.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1tYa9huYMm_ClLuvDylZvwOdg8wJKZPqm?usp=sharing)

## Notes on Accuracy

For best results, use a clear, centered, well-lit image of a single handwritten digit. Faint or low-contrast digits may produce incorrect predictions — the notebook includes a contrast-enhancement step specifically to help with this.
