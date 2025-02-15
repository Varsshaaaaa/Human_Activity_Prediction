# Human Activity Recognition (HAR) Using Deep Learning

## 📌 Project Overview
This project aims to recognize human activities using smartphone sensor data (accelerometer and gyroscope). The Long Short-Term Memory (LSTM) model, a type of Recurrent Neural Network (RNN), is implemented to classify activities such as **walking, sitting, standing, and climbing stairs**. The dataset used is the **UCI Human Activity Recognition (HAR) Dataset**.

## 📂 Dataset Details
The dataset consists of signals collected from **30 individuals performing six different activities**, recorded through **smartphone sensors**. Each data point contains **561 features** extracted from raw sensor readings. Link to dataset:https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones

### Dataset Structure:
- **train/** - Training data
- **test/** - Testing data
- **features.txt** - Names of 561 features
- **activity_labels.txt** - Mapping of activity IDs to labels
- **subject_train.txt** - Subject IDs for training data
- **subject_test.txt** - Subject IDs for test data
- **y_train.txt / y_test.txt** - Activity labels for training/testing

## 🔧 Preprocessing Steps
1. **Data Cleaning** - Removed missing or corrupted values.
2. **Feature Scaling** - Applied StandardScaler to normalize data.
3. **Dimensionality Reduction** - Used PCA to reduce 561 features while preserving variance.
4. **Class Balancing** - Used SMOTE to handle imbalanced activity classes.
5. **Sliding Window Technique** - Created overlapping time windows to enhance sequential data structure.

## 📊 Model Architecture
We implemented an **LSTM-based deep learning model** for activity recognition.

### **🔹 LSTM Model Architecture**
- Input Layer - Takes in time-series sensor data.
- **LSTM Layers** - Captures temporal dependencies.
- **Dropout Layers** - Prevents overfitting.
- **Dense Layer** - Fully connected layer for classification.
- **Softmax Activation** - Outputs probabilities for each activity class.

## 📈 Performance Metrics
- **Accuracy**: 94.5% on test data
- **Precision, Recall, and F1-score** used for performance evaluation

## 💡 Challenges Faced & Solutions
1. **High-Dimensional Data**: Used PCA and feature selection.
2. **Sensor Noise**: Applied filtering techniques.
3. **Overfitting**: Used dropout and early stopping.
4. **Deployment**: Converted to lightweight TFLite for mobile.

## 📚 Future Improvements
- Implement **Transformer-based HAR models**.
- Optimize model for **edge computing devices**.
- Experiment with **CNN-LSTM hybrid models** for improved accuracy.

## 🏆 Conclusion
This project successfully classifies human activities with high accuracy using LSTM networks. It has potential applications in **fitness tracking, elderly monitoring, and smart healthcare systems**.

