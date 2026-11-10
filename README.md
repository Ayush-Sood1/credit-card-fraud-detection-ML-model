# credit-card-fraud-detection-ML-model
Machine Learning-based Credit Card Fraud Detection and Forensic Analysis
# Credit Card Fraud Detection using Machine Learning

## Project Overview
This project builds a baseline Machine Learning model to identify potentially fraudulent credit card transactions.

The aim is to understand how Machine Learning can support fraud detection and how model predictions can be examined from a forensic perspective.

## Dataset
- Total transactions: 284,807
- Legitimate transactions: 284,315
- Fraudulent transactions: 492
- Fraud cases represent approximately 0.173% of the dataset.

The dataset contains anonymised features (`V1` to `V28`), transaction time (`Time`), transaction amount (`Amount`), and the target column (`Class`).

**Note:** The dataset file is not included in this repository. Download the dataset separately and update the file path in the notebook to match your own setup.

## Methodology
1. Explored and understood the dataset.
2. Checked for missing values and duplicate records.
3. Separated input features (`X`) and target (`y`).
4. Split the data into training and testing sets (80:20), using stratification.
5. Scaled the `Time` and `Amount` features.
6. Trained a Logistic Regression model.
7. Evaluated its performance using classification metrics and a confusion matrix.
8. Investigated missed fraud cases and their predicted fraud probabilities.

## Model Performance

| Metric | Score |
|---|---:|
| Accuracy | 99.92% |
| Precision | 82.89% |
| Recall | 64.29% |
| F1-score | 72.41% |

### Confusion Matrix

| | Predicted Legitimate | Predicted Fraud |
|---|---:|---:|
| Actual Legitimate | 56,851 | 13 |
| Actual Fraud | 35 | 63 |

The model detected 63 out of 98 fraudulent transactions in the test set and missed 35.

## Forensic Analysis
The project further examines:
- Fraudulent transactions missed by the model.
- Differences in transaction amounts between detected and missed fraud cases.
- Fraud probability scores assigned to actual fraud cases.

## Limitations
- The dataset is highly imbalanced.
- Features `V1` to `V28` are anonymised, limiting direct interpretation.
- Logistic Regression is used as a baseline model and may not capture every complex fraud pattern.
- This is an educational prototype, not a production-ready fraud detection system.

## Future Improvements
- Experiment with other Machine Learning algorithms.
- Explore techniques to handle class imbalance.
- Tune the prediction threshold.
- Compare model performance across different approaches.

## Tools and Technologies
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Disclaimer
This project is created for educational and learning purposes. Model predictions should not be treated as definitive proof of fraud.
