🧠 Artificial Neural Network for Customer Churn Prediction
📌 Overview
This project implements an Artificial Neural Network (ANN) using TensorFlow/Keras to predict whether a customer will churn (leave a service) based on their historical data. Accurate churn prediction helps companies take preventive action and retain valuable customers.

🗃️ Dataset
File: Churn_Modelling.csv

Features Used: Credit score, geography, gender, age, tenure, balance, number of products, has credit card, active member, estimated salary

Target Variable: Exited (1 = churned, 0 = retained)

🔧 Technologies Used
Python

TensorFlow / Keras

NumPy, Pandas

Scikit-learn (for preprocessing and metrics)

🧪 Steps & Methodology
Data Preprocessing

Selected relevant features (excluding RowNumber, CustomerId, Surname)

Label encoded Gender

One-hot encoded Geography

Feature scaling using StandardScaler

Split into training and testing sets (80/20)

Model Architecture

Built a Sequential ANN with:

Two hidden layers (6 units each, ReLU activation)

One output layer (1 unit, sigmoid activation)

Compiled with adam optimizer and binary_crossentropy loss

Trained on the training set for 100 epochs with batch size 32

Prediction

Evaluated model on test data

Made prediction on a single new data point

Evaluation

Used confusion_matrix and accuracy_score for performance evaluation

Confusion Matrix:
[[1523   72]
 [ 202  203]]
 
Accuracy Score:
~85% 

🧠 Example Use
To predict churn for a customer with the following data:
ann.predict(sc.transform([[1, 0, 0, 600, 1, 40, 3, 60000, 2, 1, 1, 50000]])) > 0.5
Returns: False → This customer is not likely to churn.

📂 Project Files
css
Copy
Edit
.
├── Churn_Modelling.csv
├── ann.py
├── README.md
└── requirements.txt
