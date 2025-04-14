# 1D Gaussian GAN Training

This repository contains a minimal implementation of a **Generative Adversarial Network (GAN)** designed to learn and generate samples from a **1D Gaussian distribution**.

## 📌 Project Overview

The objective is to train:
- A **Generator** that learns to produce fake samples that resemble the true Gaussian distribution.
- A **Discriminator** that learns to distinguish between real samples (from the true distribution) and fake samples (from the generator).

The training is based on **binary cross-entropy loss**, and optimization is done using **gradient descent**.

## 🧠 Key Concepts

- The **Generator** generates data \( x = z + \theta \), where \( z \sim \mathcal{N}(0, 1) \) and \( \theta \) is a learnable parameter.
- The **Discriminator** is a logistic regression model \( p(x) = \sigma(\beta_0 + \beta_1 x) \), trained to classify real vs. fake data.
- The system trains adversarially: the generator improves to fool the discriminator, while the discriminator improves to spot the fake data.

## 📁 Files

- `GEN_Training.ipynb`: Jupyter notebook with code, visualizations, and experiments.
- `gan_train.py`: Python script version of the GAN training loop for easier CLI-based usage (if applicable).
- `README.md`: This file.

## 📊 What’s Included

- Loss plots for both Generator and Discriminator across training.
- Discriminator's output probability function visualized over training epochs.
- Exploration of different learning rates and their effect.
- Bonus: Training using **Stochastic Gradient Descent (SGD)** and comparing dynamics with batch gradient descent.


## 🧪 Experiments

Try adjusting:
- Learning rates of the generator and discriminator
- Initial parameters
- Batch vs. stochastic gradient descent

Observe how these changes affect:
- Training stability
- Convergence
- Quality of generated samples

## 📌 Notes

This is a simplified GAN setup focused on concept understanding. No deep learning libraries are used — all calculations are done using NumPy for full transparency and educational clarity.

---

Happy training! 🎉
