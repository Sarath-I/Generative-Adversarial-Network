🎨 Handwritten Digit Generation using GAN (Generative Adversarial Network)




📌 Project Overview

This project implements a Generative Adversarial Network (GAN) using TensorFlow/Keras to generate realistic handwritten digit images similar to the MNIST dataset.

GANs are one of the most powerful deep learning models for generative modeling, where two neural networks — a Generator and a Discriminator — compete against each other to improve performance. This project demonstrates how adversarial learning can be used to generate high-quality synthetic data.

🎯 Objective

The main objective of this project is to design and train a GAN model capable of generating realistic handwritten digit images by learning the underlying distribution of the MNIST dataset.

🧠 What is GAN?

A Generative Adversarial Network (GAN) consists of two models:

Generator
Takes random noise as input
Generates synthetic images
Learns to fool the discriminator
Discriminator
Takes real and fake images as input
Classifies them as real (1) or fake (0)
Learns to detect fake samples

Both models are trained in a minimax game, where:

The generator improves to create realistic images
The discriminator improves to detect fake ones
📊 Dataset
MNIST Handwritten Digits Dataset
Image size: 28 × 28 (grayscale)
Data normalized to range [-1, 1]
⚙️ Model Architecture
🟢 Generator Network
Dense Layer
Batch Normalization
LeakyReLU Activation
Conv2DTranspose Layers
Output Layer with Tanh activation
🔴 Discriminator Network
Conv2D Layers
LeakyReLU Activation
Dropout
Flatten Layer
Dense Layer with Sigmoid activation
🛠️ Training Details
Loss Function: Binary Cross-Entropy (BCE)
Optimizer: Adam (lr = 0.0002, β₁ = 0.5)
Epochs: 20

The generator and discriminator are trained simultaneously to improve performance through adversarial learning.

📉 Training Insights (Loss Analysis)
The generator loss initially increases, indicating early learning struggles
Over time, it stabilizes around 0.78–0.80, showing improved image generation
The discriminator loss stabilizes around 1.30–1.32, indicating difficulty distinguishing real vs fake images

This behavior reflects a balanced GAN training process, where both networks improve together without dominance.
(Refer to the loss graph in the report, page 3)

🖼️ Generated Results
Early epochs: Noisy and unclear digit shapes
Later epochs: Clear and structured handwritten digits
Generator progressively improves realism over training epochs

(See generated image samples on page 4 of the report)

📁 Project Structure
GAN-Handwritten-Digit-Generator
│
├── notebooks
│   └── Generative_Adversarial_Network.ipynb
│
├── outputs
│   ├── loss_graph.png
│   └── generated_images.png
│
├── README.md


🛠️ Technologies Used
Python
TensorFlow / Keras
NumPy
Matplotlib
Deep Learning

📊 Results

The GAN model successfully learns the distribution of handwritten digits and generates realistic synthetic images. The adversarial training process enables continuous improvement in output quality across epochs.
