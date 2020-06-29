# GAN Implementation with Pytorch


## 0. Develop Environment
- Docker Image : tensorflow/tensorflow:1.13.2-gpu-py3-jupyter
- Pytorch : Stable (1.5) - Linux - Python - CUDA (10.2)
- Using Single GPU (not tested on cpu only)


## 1. Explain about Implementation


## 2. Brief Summary of *'Generative Adversarial Nets'*

## 2.1. Goal
- Make generative model that does not require Markov chain without designing model carefully

### 2.2. Intuition
- 2 player minmax game

### 2.3. Dataset
- MNIST
- TFD (Toronto Face Database)
- CIFAR10

### 2.4. GAN Configurations
![Figure 1](./Figures/Figure_01.png)
- 2 player minmax game with above value function V(G, D)
- Generative model G (input : noise, output : generated image)
  * Capture data distribution
  * Differentiable function represented by a multilayer perceptron
  * Activation function : mixture of rectifier linear activations and sigmoid activations
  * Noise as the input
- Discriminative model D (input : image, output : probability)
  * Estimate probability that sample came from training data rather than G
  * Differentiable function represented by a multilayer perceptron
  * Activation function : maxout acitivations
  * Dropout

### 2.5. Image Generation
- Metric : parzen window-based log-likelihood estimates


## 3. Reference Paper
- Generative Adversarial Nets [[paper]](https://arxiv.org/pdf/1406.2661.pdf)
