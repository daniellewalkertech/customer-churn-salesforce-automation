# Customer Churn Prediction + Salesforce Retention Automation

## Project Overview

This project demonstrates how machine learning predictions can be connected to Salesforce CRM automation to support customer retention.

A Python artificial neural network analyzes telecommunications customer data and predicts the likelihood of customer churn. The machine learning model is evaluated to identify both successful predictions and areas where churn detection can be improved.

The Salesforce portion of the project extends the machine learning workflow by bringing churn risk information into Salesforce Account records. Salesforce Flow can then use the predicted risk score to trigger retention actions for high-risk customers.

### End-to-End Workflow

Customer Data → Python Machine Learning Model → Churn Risk Prediction → Salesforce Account → Salesforce Flow → Retention Action

## Technologies

- Python
- Pandas
- Scikit-learn
- TensorFlow / Keras
- Google Colab
- Salesforce
- Salesforce Flow
- GitHub

## Machine Learning Results

- Dataset: 7,043 telecommunications customers
- Features used for modeling: 30
- Model: Artificial Neural Network
- Test Accuracy: 79.06%
- Churn Precision: 62%
- Churn Recall: 56%
- Churn F1-Score: 59%

### Confusion Matrix

- True Negatives: 905
- False Positives: 130
- False Negatives: 165
- True Positives: 209

## Key Finding

Although the model achieved 79.06% overall test accuracy, churn recall was 56%. The model failed to identify 165 customers who actually churned.

In a real customer retention environment, these false negatives are especially important because those customers could be missed by retention efforts. Future model development should focus on improving churn detection while monitoring the effect on false positives.

## Salesforce Automation

The Salesforce portion of this project will demonstrate how a machine learning prediction can become an actionable CRM workflow.

Planned workflow:

1. Store the predicted churn risk score on the Salesforce Account.
2. Identify accounts that exceed a defined churn-risk threshold.
3. Use a record-triggered Salesforce Flow to classify the account as high risk.
4. Automatically create a retention task for the Account Owner.
5. Track the customer's retention status in Salesforce.

## Project Status

🚧 In Development

- [x] Customer data preprocessing
- [x] Feature encoding and scaling
- [x] Neural network development
- [x] Model training
- [x] Model evaluation
- [ ] Salesforce custom fields
- [ ] Salesforce churn-risk Flow
- [ ] Prediction import into Salesforce
- [ ] End-to-end testing
