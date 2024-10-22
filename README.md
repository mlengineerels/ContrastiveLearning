# Contrastive Learning

This repository contains the implementation of contrastive learning techniques for unsupervised and self-supervised learning tasks. 
Contrastive learning has gained prominence in training deep neural networks to learn effective representations by encouraging similar (positive) samples to be closer in the embedding space and dissimilar (negative) samples to be farther apart.

## Introduction

Contrastive learning is a powerful approach for learning visual representations in an unsupervised manner. 
It has been effectively used for tasks like image classification, object detection, and clustering. 
This project implements a contrastive learning framework for representation learning, enabling deep models to better differentiate between classes based on similarity measures.

The main goal is to learn representations by using pairs of similar and dissimilar examples,
utilizing techniques like SimCLR (Simple Framework for Contrastive Learning of Visual Representations) and other advanced contrastive loss functions.

## Methodology

The project uses the contrastive loss to train a model in an unsupervised manner. 
The core idea is to bring positive samples (i.e., augmented views of the same image) closer in the embedding space while pushing apart negative samples.
The methodology is as follows:

1. **Data Augmentation**: Random augmentations such as cropping, flipping, and color distortion are applied to input data.
2. **Backbone Network**: A deep neural network (e.g., ResNet) is used to extract features from the input images.
3. **Projection Head**: A small MLP network is added to the backbone to project the learned features into a latent space where contrastive loss is applied.
4. **Contrastive Loss**: The contrastive loss function is applied, aiming to minimize the distance between positive pairs and maximize the distance between negative pairs.

Visualization of Learned Representations
The learned representations can be visualized using t-SNE or UMAP to observe how well the model separates different classes in the latent space.

##### Step by step implementation can be found in scripts/ipynb notebook



