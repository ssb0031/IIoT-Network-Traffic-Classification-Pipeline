# Enhanced IIoT Network Traffic Classification Pipeline

## 📋 Project Overview
This project implements an advanced Intrusion Detection System (IDS) for Industrial Internet of Things (IIoT) networks using machine learning and deep learning techniques. The system classifies network traffic as normal or attack traffic using multiple model architectures.

## 🎯 Features
- **Advanced Data Preprocessing**: Feature sanitization, flow-based splitting, and SMOTE balancing
- **Multiple Model Architectures**:
  - Tabular Models: RandomForest, LogisticRegression, SGD_Classifier
  - Sequential Models: LSTM, TCN with Attention, Hybrid CNN-LSTM
- **Comprehensive Evaluation**: Accuracy, AUC, F1, Precision, Recall, Latency metrics
- **Visualization Suite**: Confusion matrices, training history, performance radar charts
- **Flow-Based Splitting**: Prevents data leakage by grouping related network flows

## 📊 Dataset
- **Source**: WUSTL IIoT 2021 Dataset
- **Records**: 1,048,576 network traffic samples
- **Classes**: Normal (97.29%) vs Attack (7.71%) - Imbalanced dataset
- **Features**: 58 engineered features including temporal, protocol, and statistical metrics

## 🏗️ Model Architectures

### Sequential Models:
1. **Regularized LSTM**: Bidirectional LSTM with dropout and L2 regularization
2. **TCN-Attention**: Temporal Convolutional Network with attention mechanism
3. **Hybrid CNN-LSTM**: Combined convolutional and recurrent layers

### Tabular Models:
1. **Random Forest**: 100 estimators
2. **Logistic Regression**
3. **SGD Classifier**

## 📈 Performance
Best performing model: **LSTM_Regularized**
- **AUC**: 0.999998
- **Accuracy**: 0.999809
- **F1 Score**: 0.998688
- **Recall (Attack)**: 0.997379
- **Latency**: 1.5135 ms

## 🚀 Quick Start

### Prerequisites
```bash
Python 3.8+
TensorFlow 2.x
GPU with CUDA support (optional but recommended)