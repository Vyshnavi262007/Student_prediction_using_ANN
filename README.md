Student Career Prediction using ANN
Project Overview

This project predicts a suitable career for a student based on their skill set using an Artificial Neural Network (ANN).
The model learns from a dataset containing student skill values and their corresponding professions, and then uses this knowledge to predict careers for new inputs.

Objective

The main objective of this project is to analyze student skills and recommend an appropriate career path using machine learning techniques.

Dataset Description

The dataset is taken from an Excel file and contains the following:

Input Features
Linguistic
Musical
Bodily
Logical - Mathematical
Spatial-Visualization
Interpersonal
Intrapersonal
Naturalist
Output
Job Profession (for example: Engineer, Lawyer, Journalist, etc.)
Methodology
Data Loading

The dataset is loaded from an Excel file using the Pandas library.

Data Preprocessing
Required columns are selected
Missing values are removed
The job profession column is converted into numerical form using Label Encoding
One-hot encoding is applied for multi-class classification
Feature scaling is performed using StandardScaler
Train-Test Split

The dataset is divided into training and testing data in an 80:20 ratio to evaluate model performance on unseen data.

Model Description

An Artificial Neural Network is used with the following structure:

Input layer with 8 features
First hidden layer with 128 neurons and ReLU activation
Dropout layer to reduce overfitting
Second hidden layer with 64 neurons and ReLU activation
Output layer with Softmax activation
Training Details
Optimizer: Adam
Loss Function: Categorical Crossentropy
Epochs: 50
Batch Size: 16

The model learns patterns between input features and job professions during training.

Evaluation

The model performance is evaluated using:

Accuracy
Precision
Recall
F1-score
Classification Report

The model achieved approximately 92.5% accuracy on the test data.

Prediction Process

To predict a career:

Provide input values representing student skills
Scale the input using the trained scaler
Pass the input to the trained ANN model
The model calculates probabilities for all professions
The profession with the highest probability is selected as the output
Example

Input:
[15, 8, 12, 18, 16, 14, 17, 10]

Output:
Recommended Career Path: Engineer

Key Concepts
Artificial Neural Network
Multi-class Classification
Feature Scaling
Label Encoding and One-hot Encoding
Softmax Activation
Future Scope
Improve accuracy with larger datasets
Tune model parameters
Build a user interface for easy input
Provide multiple career suggestions instead of one
Author

Vyshnavi Ponapati
B.Tech Computer Science Engineering
