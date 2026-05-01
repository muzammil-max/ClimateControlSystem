# Assignment 03: 🌡️ Modeling a Smart Climate Control System Using a Multi-Layer Neural Network

**Course:** MT1006 Differential Equations  
**Instructor:** Miss Qurat Ul Ain
**Platform:** Google Colab  
**Framework:** PyTorch  
**Colab Link:** https://colab.research.google.com/drive/1cCSS5a6G33zeaNsXPrD1bU20CfFqfbIW?usp=sharing  

---

## 📌 Overview

This project simulates a smart climate control system using a multi-layer neural network. The model learns how environmental conditions affect cooling requirements and predicts cooling intensity in real time.

---

## 🎯 Problem Statement

We aim to model a system that predicts cooling based on environmental factors:

- Room Temperature  
- Humidity  
- Number of Occupants  
- Outdoor Temperature  

### Mathematical Formulation

$$
y = f(x_1, x_2, x_3, x_4)
$$

Where:

- \(x_1\) = Room Temperature  
- \(x_2\) = Humidity  
- \(x_3\) = Occupants  
- \(x_4\) = Outdoor Temperature  
- \(y\) = Cooling Intensity (0 to 1)

---

## 📊 Dataset Design

A synthetic dataset is generated to simulate real-world behavior.

### Cooling Equation

$$
y = 0.4x_1 + 0.2x_2 + 0.2x_3 + 0.2x_4 + \epsilon
$$

Where:

$$
\epsilon \sim \mathcal{N}(0, 0.05)
$$

### Intuition

- Higher room temperature → higher cooling  
- Higher humidity → higher cooling  
- More occupants → higher cooling  
- Higher outdoor temperature → higher cooling  

---

## 🧠 Neural Network Architecture

- Input Layer: 4 neurons  
- Hidden Layer 1: 16 neurons (ReLU)  
- Hidden Layer 2: 8 neurons (ReLU)  
- Output Layer: 1 neuron (Sigmoid)

### Activation Functions

$$
\text{ReLU}(x) = \max(0, x)
$$

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

---

## 🔁 Training Process

- Loss Function: Mean Squared Error (MSE)  
- Optimizer: Adam  

### Loss Function

$$
Loss = \frac{1}{n} \sum (y_{pred} - y_{true})^2
$$

### Optimization

$$
W \leftarrow W - \eta \nabla Loss
$$

---

## 📉 Learning Behavior

$$
Loss(t) \rightarrow \min
$$

$$
\frac{d(Loss)}{dt} \rightarrow 0
$$

This indicates convergence of the model.

---

## 📈 Results

### Actual vs Predicted

$$
\hat{y} \approx y
$$

- Strong diagonal pattern  
- Small deviation due to noise  
- High prediction accuracy  

---

## 🧪 Interactive Prediction System

### Inputs:
- Room Temperature (0–1)  
- Humidity (0–1)  
- Occupants (0–1)  
- Outdoor Temperature (0–1)  

### Output:
Cooling intensity between 0 and 1

### Example:

$$
x_1 = 0.8,\quad x_2 = 0.6,\quad x_3 = 0.5,\quad x_4 = 0.7
$$

$$
y \approx 0.6 - 0.8
$$

---

## 🛡️ Validation

- Ensures numeric input  
- Enforces range [0,1]  
- Prevents invalid predictions  

---

## 📐 Differential Equations Connection

The system can be interpreted as a dynamic model:

$$
\frac{dy}{dt} = f(x_1, x_2, x_3, x_4)
$$

Learning process:

$$
\frac{dW}{dt} = -\nabla Loss
$$

This shows the system evolving toward equilibrium.

---

## 🧠 Key Insight

Because:

$$
y = f(x) + \epsilon
$$

The model cannot reach zero loss due to irreducible noise.

---

## 🛠️ Tech Stack

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- PyTorch  

---

## 👥 Team Members

- Muzammil — 25K6533  
- Junaid — 25K6538  
- Sohaib — 25K6532  

---

## 🚀 Future Improvements

- Real-world dataset integration  
- Time-series climate modeling  
- GUI dashboard  
- Model comparisons (Linear Regression, Trees)  

---

## ✅ Conclusion

This project demonstrates a neural network-based smart climate control system that learns environmental relationships, predicts cooling intensity, and connects machine learning with differential equations.

---

## 🔗 Colab Notebook

https://colab.research.google.com/drive/1cCSS5a6G33zeaNsXPrD1bU20CfFqfbIW?usp=sharing
