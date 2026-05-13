# SGD-Classifier
## AIM:
To write a program to predict the type of species of the Iris flower using the SGD Classifier.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import Necessary Libraries and Load Data.

2.Split Dataset into Training and Testing Sets

3.Train the Model Using Stochastic Gradient Descent (SGD).

4.Make Predictions and Evaluate Accuracy

5.Generate accuracy_score, confusion_matrix,classification_report
## Program:
```
/*
Program to implement the prediction of iris species using SGD Classifier.
Developed by: Naveen M
RegisterNumber:212225230198

# Import libraries
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import SGDClassifier
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score, classification_report

# Load dataset
iris = load_iris()
X = iris.data
y = iris.target

# Feature scaling (important for SGD)
scaler = StandardScaler()
X = scaler.fit_transform(X)

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Create SGD Classifier
model = SGDClassifier(max_iter=1000, random_state=42)

# Train model
model.fit(X_train, y_train)

# Predict
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))

# Detailed report
print("\nClassification Report:\n", classification_report(y_test, y_pred))
*/
```

## Output:
<img width="663" height="291" alt="Screenshot 2026-05-13 111848" src="https://github.com/user-attachments/assets/7a003138-d287-4149-a7ef-6f5b867efea0" />



## Result:
Thus, the program to implement the prediction of the Iris species using SGD Classifier is written and verified using Python programming.
