# Federated Learning for Visual Classification

This project explores the use of **federated learning** for image classification tasks using PyTorch. The goal is to simulate a decentralized training environment where multiple clients collaborate to train a shared model — without sharing their private data.

> ⚠️ **Project Status**: This project is under active development. More features, evaluations, and improvements are coming soon.

## 🧠 What is Federated Learning?

Federated learning is a privacy-preserving machine learning approach in which multiple clients train models locally on their own data. Instead of sharing raw data, only model parameters are exchanged and aggregated on a central server.

Benefits include:
- Preserving user privacy
- Reducing communication overhead
- Enabling training across distributed, heterogeneous datasets

## 🧩 Model & Dataset

- **Backbone**: This project uses **DINO (Self-Distillation with No Labels)** — a self-supervised vision transformer — as the feature extractor.
- **Dataset**: The model is trained on **CIFAR-100**, which contains 60,000 color images (32x32) across 100 fine-grained classes.

## 🔁 Data Distribution Strategy

This project supports two data-sharing modes across clients:

- **IID (Independent and Identically Distributed)**:
  - Each client receives a balanced and random subset of the dataset.
- **non-IID (Non-Independent and Identically Distributed)**:
  - Each client receives data from only a **subset of classes**, introducing natural bias and heterogeneity similar to real-world settings.

## 📌 What This Project Does

- Simulates a federated learning setup with multiple clients.
- Performs local training using DINO-based feature extraction.
- Aggregation of client models (**federated averaging**) is currently under development.
- Supports both IID and non-IID data partitioning across clients.

## 📁 Project Files Overview
The repository contains the following Jupyter notebooks:

Centralized_model_visual_classification.ipynb
Standard implementation of centralized training using the DINO backbone.

Federated_learning_server.ipynb
Initial server-side script for federated learning — primarily supports IID data settings.

federated_model_visual_classification.ipynb
Basic federated learning client-side implementation, focused on IID data distribution.

Federated_learning_server_v2.ipynb
Advanced server implementation designed for non-IID data scenarios. Includes support for proposed methods currently under development.

federated_model_visual_classification_v2.ipynb
Updated client-side notebook tailored for non-IID data and experimental techniques. Works in tandem with the v2 server script.

## 🚀 How to Run

This project runs in **Google Colab**. No local setup is required.

### Steps:

1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. The notebook includes built-in code to:
   - Mount **Google Drive**
   - Load **CIFAR-100**
   - Simulate local training and (in future) aggregation
3. **Path setup**:
   - Users must manually configure the paths to the dataset and output directories in their own Google Drive.
   - Alternatively, contact the author to request access to shared files and folders.

> ⚠️ Be sure the required data and paths are in place before running the notebook.

## 📈 Next Steps

Planned improvements:
- Visualizations for training progress (accuracy, loss, etc.)
- Evaluation metrics (e.g., confusion matrix, per-class accuracy)
- Completion of server-side model aggregation

## 👥 Team & Contributions

This project is part of a university group assignment. Contributors include:

- [Mohammad Rahbari](https://github.com/mohammad-rahbari)
- [Andrea Grasso](https://github.com/AndrewTurin)
- [Valerio Vacirca](https://github.com/AstroVale5)
- [Xin Pan](https://github.com/CheckMan1707)

## 🤝 Contributing

Suggestions, issues, and pull requests are welcome. Feel free to fork the repo and explore.

## 📬 Contact

For questions or access to required files, please contact [Mohammad Rahbari](https://github.com/mohammad-rahbari).

## 📝 Acknowledgments
This README file was created with the assistance of MML (ChatGPT) to ensure clarity, completeness, and structure.
