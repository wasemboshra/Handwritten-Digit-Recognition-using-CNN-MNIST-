# Handwritten Digit Recognition using CNN (MNIST)

## 1. Problem Description
This project focuses on recognizing handwritten digits (numbers from 0 to 9) from the official MNIST dataset. The solution is implemented using a Deep Learning approach with a Convolutional Neural Network (CNN) architecture built via TensorFlow and Keras to satisfy the course project requirements.

---

## 2. Dataset Link
The dataset is loaded directly from Keras datasets, but the formal source, documentation, and original benchmarking can be accessed here:
* **Official Source:** [MNIST Dataset Description](https://yann.lecun.com/exdb/mnist/)

---

## 3. Results (Structured Comparison Table)
Two mandatory experiments were successfully conducted by fixing the model architecture and varying the **Optimizer** and **Learning Rate (LR)**. Both models were trained over 5 epochs with a 20% validation split.

Here is the structured performance table evaluated on the standalone testing dataset (10,000 images):

| Model | Accuracy | Loss |
| :--- | :---: | :---: |
| **Model A (Adam Optimizer, LR=0.001)** | **99.18%** | **0.0263** |
| **Model B (SGD Optimizer, LR=0.01)** | **97.15%** | **0.0952** |

### Analysis:
* **Model A (Adam)** showed superior performance achieving an exceptional accuracy of **99.18%**. Adam adapts its learning rate dynamically for each parameter, leading to much faster convergence and lower loss value (**0.0263**).
* **Model B (SGD)** achieved a good accuracy of **97.15%** but fell slightly behind Model A within the 5 training epochs. Stochastic Gradient Descent uses a fixed learning rate, meaning it typically requires more epochs to converge to the same optimal weights.

---

## 4. Project Structure & Requirements Checklist
All mandatory constraints provided in the Deep Learning project guidelines are completely fulfilled:
- [x] **Data Preprocessing:** Input images normalized (scaled between 0 and 1) and reshaped to 4D tensors `(28, 28, 1)` to define the grayscale channel. Target labels encoded using One-Hot encoding.
- [x] **Model Architecture:** Implemented a Convolutional Neural Network (CNN) featuring `Conv2D` layers for feature extraction and `MaxPooling2D` for downsampling.
- [x] **Model Enhancement:** Applied a **Dropout** layer (rate = 0.2) after the dense hidden layer to improve regularization and prevent overfitting.
- [x] **Loss & Performance Monitoring:** `Categorical Crossentropy` loss function applied while utilizing a 20% validation split to monitor metrics.
- [x] **Visualization:** Training vs Validation loss and accuracy curves plotted.

---

## 5. Instructions for Running the Project
To reproduce the experiment results, execute the following steps inside your Python environment or Google Colab notebook:

1. Clone this repository to your local machine.
2. Install the necessary dependencies:
   ```bash
   pip install tensorflow numpy matplotlib
