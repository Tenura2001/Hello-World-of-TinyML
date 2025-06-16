# 🌟 TinyML: Hello World - Predict `y = sin(x)` on Microcontrollers

This project demonstrates how to build and deploy a minimal **Tiny Machine Learning (TinyML)** application on a microcontroller using **TensorFlow Lite for Microcontrollers (TFLM)**. The model learns to predict the function `y = sin(x)` in real-time, directly on the edge device.

---

## 🎯 Project Overview

This is a classic **Hello World** example for embedded machine learning. It involves training a simple neural network in Python and deploying it on a resource-constrained microcontroller using TFLM.

> ✅ Ideal for beginners exploring AI on embedded systems.

---

## 📌 Features

- ✅ Runs an ML model on low-power microcontrollers (TinyML).
- ✅ Uses **TensorFlow Lite for Microcontrollers (TFLM)** for deployment.
- ✅ Predicts a basic mathematical function: `y = sin(x)`.
- ✅ Compatible with popular microcontrollers like:
  - Arduino Nano 33 BLE Sense
  - ESP32
  - STM32
  - Arduino UNO (with optimizations)

---

## 🛠 Hardware Requirements

- ✅ Arduino Nano 33 BLE Sense *(recommended)*  
- ✅ ESP32 / STM32 board  
- ✅ Breadboard, jumper wires  
- ✅ USB cable to connect device

---

## 📦 Software Requirements

- [x] Python 3.x  
- [x] TensorFlow + TFLite Micro  
- [x] Arduino IDE  
- [x] Arduino TensorFlow Lite Library  
- [x] numpy, matplotlib (for visualization)  

---

## 🧠 Model Architecture

A small fully connected neural network:

```text
Input (1D) → Dense(16) → ReLU → Dense(16) → ReLU → Dense(1)
````

Trained to approximate the sine function (`y = sin(x)`), with x in the range `[0, 2π]`.

---

## 📁 Project Structure

```bash
tinyml-hello-world/
├── notebook/
│   └── train_sin_model.ipynb   # Train the model using TensorFlow
├── arduino/
│   └── sin_model_deploy.ino    # Arduino sketch with weights & inference
├── model/
│   └── model.tflite            # (Optional) exported model file
├── README.md                   # This file
```

---

## 🚀 How to Run

### 🔧 Step 1: Train Model in Python

1. Open `train_sin_model.ipynb` in Jupyter/Colab.
2. Run all cells to train a simple neural network.
3. At the end, extract the **weights** and **biases** for each layer.

### ⚙️ Step 2: Deploy to Microcontroller

1. Open `sin_model_deploy.ino` in Arduino IDE.
2. Replace the placeholders with the **weights and biases** copied from the notebook.
3. Upload the sketch to your microcontroller.

> 📌 Tip: Use Serial Monitor to visualize predicted output.

---

## 📊 Sample Output

```text
Input x: 1.57
Predicted y = 0.999
Actual y = 1.000
```

---

## 🤖 Demo

<img src="docs/demo-gif.gif" alt="TinyML Sine Wave Prediction Demo" width="500"/>

---

## 📚 Learn More

* [TensorFlow Lite for Microcontrollers](https://www.tensorflow.org/lite/microcontrollers)
* [Arduino TensorFlow Lite Library](https://github.com/tensorflow/tflite-micro-arduino-examples)
* [TinyML Book (MIT Press)](https://www.tinymlbook.com/)

---

## 🧠 Credits

* Inspired by TensorFlow's official [TinyML Hello World Example](https://github.com/tensorflow/tflite-micro/tree/main/tensorflow/lite/micro/examples/hello_world)

---


