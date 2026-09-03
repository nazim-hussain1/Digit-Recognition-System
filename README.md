# Digit Recognition System

A Convolutional Neural Network (CNN) that classifies handwritten digits (0–9), trained on the MNIST dataset using TensorFlow/Keras. Includes a custom preprocessing pipeline to run predictions on your own uploaded digit images, not just the MNIST test set.

## Overview

This project loads and preprocesses the MNIST dataset, trains a CNN classifier, and then applies the trained model to custom handwritten digit images — with a contrast-enhancement step to improve accuracy on real-world photos, which tend to be noisier and less centered than MNIST's clean training data.

## Model Architecture
