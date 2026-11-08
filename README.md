
# Problem Statement:  
Predict whether a client will subscribe to a bank term deposit

## Dataset Description

- This is a Bank Term Deposit Subscription Prediction dataset.
- This dataset contains information about clients of a Portuguese banking institution. The goal is to predict whether a client will subscribe to a bank term deposit (`y` variable). The data was obtained from a direct marketing campaign, and each entry corresponds to a single client.
- The dataset contains **45,211 entries** with **17 attributes**. The attributes represent client information and campaign details and include both categorical and numerical data.
- **Target Variable (`y`)**: Indicates whether the client subscribed to a term deposit (binary: `"yes/y"` or `"no/n"`).

GITHUB repo link

[GitHub Repository](https://github.com/SHILPA2026aj05583/ML/)

Comparison Table with the evaluation metrics
------------------------------------------------

## Model Performance Comparison

| ML Model Name | Accuracy | AUC | Precision | Recall | F1 Score | MCC |
|--------------|----------|----------|----------|----------|----------|----------|
| Logistic Regression | 0.901250 | 0.905574 | 0.644483 | 0.347826 | 0.451811 | 0.426058 |
| Decision Tree | 0.874599 | 0.701457 | 0.464880 | 0.475425 | 0.470093 | 0.399021 |
| KNN | 0.896163 | 0.827721 | 0.599002 | 0.340265 | 0.433996 | 0.400128 |
| Naive Bayes | 0.854805 | 0.810095 | 0.405904 | 0.519849 | 0.455864 | 0.377358 |
| SVM | **0.904899** | 0.903658 | **0.687500** | 0.343100 | 0.457755 | **0.441993** |


# Observation about model performance
## Logistic Regression	: 
Achieved the best overall balance, recording the highest AUC Score (0.905574), F1 Score (0.4518), and MCC Score (0.4260), along with a strong accuracy of ~90%.
Logistic regression handles the linear boundaries of the scaled continuous and encoded categorical features extremely well, making it the most reliable and robust model among the choices for this dataset. 


## Decision Tree	: 
Showed moderate accuracy (87.45%) with a relatively lower AUC Score (0.7014). However, it achieved a better balance between precision and recall
Prone to overfitting on complex tabular categorical unless properly tuned, but useful when a higher capture rate (recall) of positive classes is desired at the cost of precision

## KNN	: 
Performed solidly with an accuracy of 89.61% and an AUC of 0.8277. However, its recall (0.3402) dropped compared to logistic regression.  KNN captures local patterns well, but distance calculations across high-dimensional one-hot encoded categorical columns limit its discriminative power for minority classes.

## Naive Bayes	: 
Recorded the lowest accuracy (85.48%) and precision (0.4059), though it achieved a decent recall of 0.5198. The "naive" assumption of feature independence is heavily violated here due to correlations between financial balances, employment types, and historical marketing outcomes, reducing its overall efficacy.

## SVM	:  
Secured the highest Accuracy (90.04%) and Precision (0.6875), closely rivalling Logistic Regression on AUC (0.9048). Its recall was lower at 0.3431.
SVM excels at finding optimal hyperplanes to separate the classes cleanly (yielding high precision), though it is computationally expensive and slightly conservative on predicting the minority positive class.

### Best Performing Model

Based on the evaluation metrics, **SVM** achieved the highest Accuracy (**90.49%**), Precision (**68.75%**), and MCC (**0.442**), making it the best overall model for this Bank Term Deposit Subscription Prediction task.
