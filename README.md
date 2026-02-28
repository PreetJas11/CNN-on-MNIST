# 🧠 CNN on MNIST — Handwritten Digit Classifier

A beginner-friendly deep learning project that builds a Convolutional Neural Network (CNN) in Keras to classify handwritten digits (0–9) from the MNIST dataset.

---

## What's Inside

The notebook walks through the full ML pipeline:

1. **Data Loading & Exploration** — load MNIST, visualize random digits, check class distribution
2. **Data Preparation** — reshape, normalize, one-hot encode labels
3. **Model Building** — two CNN architectures (simple → deeper 3-layer CNN)
4. **Training** — compared Adadelta vs Adam optimizers
5. **Evaluation** — accuracy/loss curves, test set evaluation
6. **Feature Map Visualization** — see what Conv1 and Conv2 layers "see"

---

## Model Architecture

```
Input (28x28x1)
  → Conv2D(32) + MaxPool
  → Conv2D(64) + MaxPool
  → Conv2D(128) + MaxPool
  → Flatten
  → Dense(128) + Dropout(0.2)
  → Dense(10, softmax)
```

Trained for **24 epochs** with **Adam (lr=1e-4)** optimizer and categorical cross-entropy loss.

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Sequential_API-red?logo=keras)
![NumPy](https://img.shields.io/badge/NumPy-array_ops-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-visualization-blue)

---

## Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/cnn-mnist.git
cd cnn-mnist
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook CNN_Model_on_Mnist_Dataset.ipynb
```

> MNIST dataset is auto-downloaded via `tensorflow.keras.datasets.mnist` — no manual download needed.

---

## Results

| Optimizer | Epochs | Test Accuracy |
|-----------|--------|--------------|
| Adadelta  | 24     | ~98%+        |
| Adam (1e-4) | 24   | ~99%+        |

Training and validation loss/accuracy curves are plotted at the end of the notebook.

---

## Project Structure

```
cnn-mnist/
├── CNN_Model_on_Mnist_Dataset.ipynb   # Main notebook
├── requirements.txt                    # Dependencies
├── .gitignore                          # Files to exclude
└── README.md
```

---

## License

MIT
