# Customer Churn Prediction 📊
Overview
This project focuses on predicting customer churn using machine learning. It involves data preprocessing, model training, and evaluation to identify customers likely to churn. The model is built with TensorFlow and Keras, while data manipulation and visualization are handled using Pandas, scikit-learn, and Matplotlib.

## 📋 Table of Contents
    •	Overview
    •	Technologies Used
    •	Setup
    •	Data
    •	Model
    •	Evaluation
    •	Usage

## 🔧 Technologies Used
    •	TensorFlow 🧠: For building and training the neural network model.
    •	Keras 🏗️: High-level API for creating neural network layers.
    •	Pandas 📊: Data manipulation and preprocessing.
    •	scikit-learn 🔬: For model evaluation and metrics.
    •	Matplotlib 📈: For visualizing data and evaluation metrics.
    •	Seaborn 🌈: For enhanced data visualization.
    
## ⚙️ Setup
  Prerequisites
   Install the required Python packages:
   
    pip install tensorflow numpy pandas scikit-learn seaborn matplotlib
    
## Data 📂
The dataset includes customer details such as:

    •	Tenure
    
    •	Monthly Charges
    
    •	Customer Service Features
    
## 🧠 Model
  A neural network model with the following architecture:
    
  •	Input Layer: Dense layer with 26 neurons, ReLU activation function.

  •	Hidden Layer: Dense layer with 15 neurons, ReLU activation function.

  •	Output Layer: Dense layer with 1 neuron, Sigmoid activation function.
    
    from tensorflow.keras.models import Sequential
    from tensorflow.keras.layers import Dense

    model = Sequential([
      Dense(26, input_shape=(26,), activation='relu'),
      Dense(15, activation='relu'),
      Dense(1, activation='sigmoid')
      ])
      
## 📈 Evaluation
The model is evaluated using:
    
    • Confusion Matrix: To visualize model performance.
    
    • Classification Report: Provides precision, recall, and F1-score metrics.
    
    from sklearn.metrics import confusion_matrix, classification_report
    
    import seaborn as sns
    
    import matplotlib.pyplot as plt

# Assuming `yp` contains predictions and `y_test` contains actual values
    cm = confusion_matrix(y_test, y_pred)
    plt.figure(figsize=(10, 7))
    sns.heatmap(cm, annot=True, fmt='d', cmap='Blues')
    plt.xlabel('Predicted')
    plt.ylabel('Truth')
    plt.title('Confusion Matrix')
    plt.show()
    print(classification_report(y_test, y_pred))
    
## 🏃♂️ Usage
    To train and evaluate the model, run:
    python main.py


