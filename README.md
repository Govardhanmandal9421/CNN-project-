# MNIST Digit Classification: Comparative Analysis of Neural Network Architectures

## 📌 Project Overview
This repository contains a Google Colab notebook that explores handwritten digit classification using the widely recognized MNIST dataset. The project implements, compares, and evaluates three different machine learning and deep learning models using **TensorFlow** and **Keras** to demonstrate the evolution of model complexity and its impact on predictive accuracy.

## 🚀 Features
* **Data Preprocessing:** Includes pixel scaling (normalization by 1/255) and one-hot encoding of categorical labels.
* **Progressive Complexity:** Progresses from a simple linear baseline to a deep convolutional network.
* **Performance Evaluation:** Compares models side-by-side using a Pandas DataFrame.
* **Data Visualization:** Utilizes Seaborn and Matplotlib to plot an accuracy hierarchy for intuitive comparison.

## 🛠️ Technologies Used
* **Python** 
* **TensorFlow / Keras** (Model building and training)
* **Scikit-learn** (Metrics and evaluation)
* **Pandas** (Data manipulation and performance tracking)
* **Matplotlib & Seaborn** (Data visualization)

## 🧠 Model Architectures & Results

The models were trained on 28x28 grayscale images of handwritten digits (0-9). The comparative results are as follows:

| Model | Architecture Highlights | Test Accuracy |
| :--- | :--- | :--- |
| **Single-layer Perceptron** | Linear baseline model, Softmax activation | ~91.55% |
| **Artificial Neural Network (ANN)** | Multi-Layer Perceptron (128 and 64 ReLU dense units) | ~97.70% |
| **Convolutional Neural Network (CNN)**| 2x Conv2D layers, MaxPooling2D, Dropout (0.5) | **~99.29%** |

*Note: Minor accuracy variations may occur depending on hardware and random seed initializations during training.*

## 💻 How to Run
1. Open the notebook in [Google Colab](https://colab.research.google.com/) or your local Jupyter environment.
2. Ensure you have the required libraries installed (`pip install tensorflow pandas matplotlib seaborn scikit-learn`).
3. Run the cells sequentially to download the dataset, train the models, and generate the evaluation plots.

## 📈 Conclusion
The results clearly demonstrate the superiority of Convolutional Neural Networks for computer vision tasks. While the standard ANN performs well, the CNN's ability to extract spatial hierarchies of features allows it to achieve near-perfect accuracy on the MNIST dataset.
