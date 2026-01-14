# 🧠 CIFAR-10 Object Recognition using ResNet50

## 📌 Introduction
This project implements a deep learning–based object recognition system using the CIFAR-10 dataset and a ResNet50 convolutional neural network.  
Transfer learning is applied by leveraging a ResNet50 model pre-trained on ImageNet for feature extraction, followed by custom classification layers.

---

## 🗂 Dataset Details

- **Dataset Name:** CIFAR-10
- **Total Images:** 60,000
- **Training Images:** 50,000
- **Testing Images:** 10,000
- **Number of Classes:** 10
- **Image Size:** 256 × 256 × 3

**Classes:**
* Airplane
* Automobile
* Bird
* Cat
* Deer
* Dog
* Frog
* Horse
* Ship
* Truck

---

## ⚙️ Model Architecture

### Convolutional Base (ResNet50)

```python
convolutional_base = ResNet50(
    weights='imagenet',    # Pre-trained on ImageNet
    include_top=False,     # Top classification layers removed
    input_shape=(256, 256, 3) # Used as a feature extractor
)
convolutional_base.summary()
```

### 🧩 Custom Classification Head

* **Global Average Pooling layer**
* **Fully Connected (Dense) layers**
* **Softmax output layer** for multi-class classification

---

### 🔢 Model Configuration

* **Model Type:** Convolutional Neural Network (CNN)
* **Base Architecture:** ResNet50
* **Number of Parameters:** Pre-trained + trainable dense layers
* **Number of Classes:** 10
* **Activation Function (Output Layer):** Softmax

---

### 🧪 Training Details

* **Number of Epochs:** 10
* **Batch Size:** 32
* **Optimizer:** Adam
* **Loss Function:** Categorical Cross-Entropy

---

### ⏱ Training Performance

* **Total Training Time:** ~40 seconds
* **Processing Speed:** ~124 ms/step
* **Final Training Loss:** 0.2318
* **Final Training Accuracy:** 93.86%

---

### 📈 Evaluation Summary

* **High classification accuracy** on CIFAR-10
* **Low training loss**
* **Effective feature extraction** using transfer learning
* **Stable convergence** within limited epochs

---

### 🧠 Deep Learning Concepts Used

* **Convolutional Neural Networks (CNN)**
* **Residual Networks (ResNet)**
* **Transfer Learning**
* **Feature Extraction**
* **Multi-class Image Classification**

---

### 📁 Project Files

* **CIFAR10_ResNet50.ipynb**
    * Data preprocessing
    * Model construction
    * Training and evaluation
    * Performance analysis

---

### 🚀 Conclusion

The use of **ResNet50 with transfer learning** enables efficient and accurate object recognition on the CIFAR-10 dataset. This project demonstrates how deep convolutional models can achieve strong performance with limited training time.
