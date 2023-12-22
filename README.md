# Conditional Image Generation with GANs for Biomedical Data Augmentation

## Overview

This repository contains the implementation of a Conditional Generative Adversarial Network (cGAN) for image generation, specifically designed for biomedical data augmentation. The project focuses on generating synthetic biomedical images to overcome challenges related to limited and diverse datasets in the medical domain.

## Table of Contents

- [Introduction](#introduction)
- [Environment Setup](#environment-setup)
- [Data Loading and Preprocessing](#data-loading-and-preprocessing)
- [Model Architecture](#model-architecture)
  - [Weight Initialization](#weight-initialization)
  - [Generator Network](#generator-network)
  - [Discriminator Network](#discriminator-network)
- [Training Strategy](#training-strategy)
  - [Loss Function and Optimizers](#loss-function-and-optimizers)
  - [Training Loop](#training-loop)
  - [Performance Metrics](#performance-metrics)
- [Output Interpretation](#output-interpretation)
- [Conclusion](#conclusion)

## Introduction

Biomedical imaging is crucial for medical research and diagnosis, but limited annotated datasets pose challenges for machine learning models. This project leverages cGANs to generate synthetic biomedical images for data augmentation. Two datasets, MNIST and CelebA, are used to showcase the model's versatility.

## Environment Setup

- Use GPU if available (`cuda`).
- Set the number of workers for the data loader (`workers`).
- Configure batch size, image size, and other hyperparameters in `config.py`.

## Data Loading and Preprocessing

- MNIST dataset: Grayscale handwritten digits.
- CelebA dataset: Color images of celebrity faces.
- Preprocessing involves resizing, normalization, and transformations.

## Model Architecture

### Weight Initialization

- Weight initialization function for stable training.

### Generator Network

- Transpose convolutional layers for generating synthetic images.
- Conditional information is incorporated for targeted synthesis.

### Discriminator Network

- Convolutional layers for binary classification of real and generated images.
- Leaky ReLU activations and batch normalization for stability.

## Training Strategy

### Loss Function and Optimizers

- Binary Cross Entropy (BCE) loss for discriminator and generator.
- Adam optimizers for efficient gradient-based optimization.

### Training Loop

- Alternating updates for discriminator and generator.
- Key performance metrics include Loss\_D, Loss\_G, D(x), and D(G(z)).

### Performance Metrics

- Loss\_D: Discriminator loss.
- Loss\_G: Generator loss.
- D(x): Average output of discriminator for real batch.
- D(G(z)): Average discriminator outputs for fake batch.

## Output Interpretation

- Interpretation of training loop output metrics.
- Understanding Loss\_D, Loss\_G, D(x), and D(G(z)).

## Conclusion

In conclusion, this project demonstrates the implementation and training of a cGAN for biomedical data augmentation. The model's ability to conditionally generate images with specific attributes enhances its adaptability to different biomedical applications.

## Contributors

- [Your Name]
- [Other contributors, if any]

## License

This project is licensed under the African Masters in Machine Intelligence.

