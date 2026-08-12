# Fraud Detection Project
**Objective:** Build a machine learning model to detect fraudulent financial transactions and learn how to handle highly imbalanced datasets.

## 1. The Challenge: Imbalanced Data
The hardest part about fraud detection is that in the real world, 99% of transactions are legitimate and only 1% are fraud. 
If we don't fix this "Class Imbalance", an AI can just guess "Not Fraud" every time, get 99% accuracy, but fail to catch any actual criminals!

## 2. Exploring the Data (EDA)
Before building models, I checked the data to find patterns:
* **Transaction Amounts:** I looked at the distribution to see if fraudsters spend different amounts than normal people.
* **Time of Day:** I created charts to see if frauds happen at specific hours.

## 3. Preparing the Data
Machine learning models only understand numbers.
* I used **One-Hot Encoding** to convert text categories (like merchant types) into 1s and 0s.
* I split the data into training (80%) and testing (20%) sets, ensuring the same percentage of fraud was in both sets using stratification.

## 4. Fixing the Imbalance (SMOTE)
To give the AI enough "bad guys" to study, I used a technique called **SMOTE** (Synthetic Minority Over-sampling Technique).
* SMOTE analyzes the few fraud cases we have and generates **new, synthetic, but highly realistic fraud examples**.
* Now the training data is perfectly balanced 50/50!

## 5. Training Models
I trained and compared two different AI models to see which was smarter:
1. **Logistic Regression:** A classic, fast statistical model.
2. **Random Forest:** A more powerful algorithm that builds hundreds of decision trees.

## 6. Evaluating Success
Because standard "Accuracy" is misleading, I evaluated the models using better metrics:
* **Recall:** Out of all actual frauds, how many did we catch? (Crucial for minimizing financial loss).
* **Precision:** When the model guessed fraud, how often was it right? (Important so we don't block valid customers).
* **AUC-ROC Curve:** A graph showing the trade-off between catching criminals and blocking legitimate users.

## 7. Inside the AI's Brain
I extracted **Feature Importance** from the Random Forest model to see exactly which clues or columns the AI relied on the most when making its decisions.

## 8. Final Output
The notebook successfully demonstrates how to train a fraud detection model on imbalanced data, ready to be scaled for real-world transaction streaming!
