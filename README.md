# 🧠 Handwritten Digit Classification: Neural Network Benchmark on MNIST

[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)](https://keras.io/)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Open in Colab](https://img.shields.io/badge/Open_In_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/github/Govardhanmandal9421/CNN-project-/blob/main/CNN%20project.ipynb)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Govardhan_Mandal-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/govardhan-mandal-268121440/)

A deep learning comparative benchmark evaluating three distinct neural network architectures on 70,000 grayscale samples of the **MNIST handwritten digit dataset**: Single-Layer Perceptron, Multi-Layer Artificial Neural Network (ANN), and a Deep Convolutional Neural Network (CNN).

---

## 🏆 Architecture Comparison & Benchmark Results

| Model Architecture | Layer Details | Parameters | Test Accuracy | Overfitting Control |
|--------------------|---------------|------------|---------------|---------------------|
| **Single-Layer Perceptron** | Dense(10, Softmax) | ~7.8K | **91.50%** | Baseline Linear Model |
| **Multi-Layer ANN** | Dense(128, ReLU) + Dense(10, Softmax) | ~101K | **97.70%** | Non-linear activation |
| **Convolutional Neural Network (CNN)** | Conv2D(32) + MaxPool + Conv2D(64) + Dense(128) + Dropout(0.25) | ~1.2M | **99.30%** | Dropout + Spatial Convolutions |

---

## 🔬 CNN Architecture Breakdown

```text
Input (28x28x1 Grayscale Image)
       │
       ▼
Conv2D (32 filters, 3x3 kernel, ReLU activation) ──► Output shape: (26, 26, 32)
       │
       ▼
MaxPooling2D (2x2 pool size) ──► Output shape: (13, 13, 32)
       │
       ▼
Conv2D (64 filters, 3x3 kernel, ReLU activation) ──► Output shape: (11, 11, 64)
       │
       ▼
MaxPooling2D (2x2 pool size) ──► Output shape: (5, 5, 64)
       │
       ▼
Flatten Layer (1600 nodes)
       │
       ▼
Dense Hidden Layer (128 units, ReLU activation)
       │
       ▼
Dropout Regularization (rate = 0.25 to prevent co-adaptation)
       │
       ▼
Dense Output Layer (10 units, Softmax activation) ──► Class Probabilities (Digits 0-9)
```

---

## ⚡ Training Configuration

* **Optimizer:** Adam ($lpha = 0.001$, $eta_1 = 0.9$, $eta_2 = 0.999$)
* **Loss Function:** Categorical Cross-Entropy
* **Batch Size:** 128
* **Epochs:** 15 (with Early Stopping callback)
* **Dataset:** 60,000 Training Samples, 10,000 Test Samples (Normalized to $[0, 1]$)

---

## 📂 Repository Contents

* `CNN project.ipynb` — Complete Google Colab / Jupyter Notebook including data preprocessing, model compilation, training histories (loss/accuracy curves), and confusion matrices.
* `README.md` — Project documentation and benchmark analysis.

---

## 👨‍💻 Author & Connect

* **Developer:** Govardhan Mandal
* **Portfolio:** [govardhanmandal9421.github.io](https://govardhanmandal9421.github.io)
* **LinkedIn:** [linkedin.com/in/govardhan-mandal-268121440](https://www.linkedin.com/in/govardhan-mandal-268121440/)
* **GitHub:** [github.com/Govardhanmandal9421](https://github.com/Govardhanmandal9421)
