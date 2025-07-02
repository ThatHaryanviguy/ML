# 🧬 Unsupervised Learning on Gene Expression Data

This project explores the use of autoencoders for dimensionality reduction and clustering of gene expression profiles using Keras and scikit-learn.

The goal is to learn compressed latent representations of 23-dimensional gene expression data and evaluate how well they preserve biological structure using clustering metrics such as the Davies–Bouldin Index (DBI).

---

## 🔍 Problem Statement

High-dimensional gene expression data is difficult to analyze directly due to noise and the curse of dimensionality. This project uses:

- A simple feedforward autoencoder to compress gene expression vectors
- KMeans and Gaussian Mixture Models to cluster samples in the latent space
- DBI scores and t-SNE visualizations to assess cluster quality

---

## 📦 Dataset

- Source: [Kaggle Dataset – Gene Expression Bioinformatics Dataset](https://www.kaggle.com/datasets/samira1992/gene-expression-bioinformatics-dataset)
- Samples: Rows represent different patient samples
- Features: 23 gene expression values per sample

---

## 🧠 Model Architecture

- Input dimension: 23
- Encoder: 3-neuron hidden layer with ReLU
- Decoder: Dense layer reconstructing the 23 features
- Loss function: Binary crossentropy / MSE
- Optimizer: Adam
- Training: 50 epochs, batch size = 250


Optional deeper variants were explored by stacking additional dense layers before and after the bottleneck.
