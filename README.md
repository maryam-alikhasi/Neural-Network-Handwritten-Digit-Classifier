# Neural-Network-Handwritten-Digit-Classifier

This project implements a **multiclass neural network** using TensorFlow and Keras to recognize **handwritten digits (0–9)**. The data comes from a subset of the MNIST dataset.

This practice lab is part of a [Coursera Machine Learning course](https://www.coursera.org/), focusing on multiclass classification with neural networks.

---

## Project Summary

- **Input**: 20x20 grayscale images of digits (flattened to 400 features).
- **Output**: 10-class classification (digits 0 to 9).
- **Model**: 3-layer fully connected neural network.
- **Activation Functions**:
  - Hidden Layers: ReLU
  - Output Layer: Linear (with softmax applied via `from_logits=True`)
- **Loss Function**: SparseCategoricalCrossentropy
- **Optimizer**: Adam
- **Framework**: TensorFlow / Keras

---

## Model Architecture

| Layer      | Type       | Units | Activation |
|------------|------------|-------|------------|
| Input      | Dense      | 400   | -          |
| Hidden 1   | Dense      | 25    | ReLU       |
| Hidden 2   | Dense      | 15    | ReLU       |
| Output     | Dense      | 10    | Linear + Softmax (via loss) |

---

## Dataset
- **Source**: Subset of MNIST  
- **Size**: 5000 examples  
- **Shape**:
  - `X`: (5000, 400)
  - `y`: (5000, 1)
---

## Training Configuration

- **Epochs**: 40
- **Batch Size**: Default (32)
- **Loss** is tracked and plotted using `history.history['loss']`.

---


## Acknowledgments

* Course: Machine Learning Specialization – [DeepLearning.AI]
* Dataset: [MNIST Subset](http://yann.lecun.com/exdb/mnist/)
* Framework: [TensorFlow](https://www.tensorflow.org/)
