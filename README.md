# Neural Network Cancer Severity Analysis (2015–2024)

This project applies an artificial neural network model to predict cancer severity based on clinical, behavioral and environmental risk factors using patient-level data from 2015 to 2024.

## Objective

The objective of this project is to develop and evaluate a multilayer perceptron neural network for predicting cancer severity and to analyze how demographic, genetic, behavioral and environmental variables influence disease severity.

## Dataset

The dataset used in this project is the Global Cancer Patients (2015–2024) dataset, publicly available on Kaggle. It contains patient-level information from multiple countries, including demographic, genetic, behavioral and environmental factors associated with cancer severity.

Dataset source:  
https://www.kaggle.com/datasets/zahidmughal2343/global-cancer-patients-2015-2024

## Approach

The analysis starts with data cleaning and feature selection to ensure that only variables directly related to cancer severity are used. Variables such as treatment cost, survival years, country and cancer type were removed to avoid data leakage and structural bias. Numerical features were normalized using MinMaxScaler, and categorical variables were encoded using One Hot Encoding.

A multilayer perceptron neural network was implemented for a regression task, allowing the model to capture non-linear relationships between risk factors and the cancer severity score.

## Neural Network Architecture

The model consists of a fully connected neural network with two hidden layers using ReLU activation functions and a linear output layer. The network was trained using the Adam optimizer and Mean Squared Error as the loss function. Training was performed with an 80/20 train-test split.

The number of training epochs was reduced from 200 to 30 based on the stabilization of the loss curve, improving computational efficiency and reducing the risk of overfitting.

## Evaluation Metrics

Model performance was evaluated using regression metrics, including Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE) and R² score.

## Results

The neural network demonstrated stable convergence and similar performance on training and test sets. The model achieved R² values close to 0.79 on the training set and 0.78 on the test set, indicating good generalization capability. Loss curves showed no divergence between training and validation, and prediction plots revealed strong alignment between real and predicted severity values.

Feature importance analysis based on network weights indicated that genetic risk and smoking were the most influential variables, followed by obesity level, air pollution exposure, alcohol use and age.

## Conclusion

The results demonstrate that neural networks are an effective approach for predicting cancer severity and for modeling complex non-linear relationships between clinical, behavioral and environmental risk factors. The findings reinforce the relevance of genetic predisposition and lifestyle factors in disease severity and highlight the potential of neural networks to support risk analysis and decision-making in healthcare contexts.

How to Run

Install dependencies:

pip install -r requirements.txt

Open the notebook:

02_machine_learning_cancer_severity_analysis_2015_2024.ipynb

You can run it locally or directly in Google Colab using the Open in Colab button.

