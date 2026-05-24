# ML Output Evaluator
A reusable end-to-end notebook for evaluating machine learning
model outputs. Built as part of an AI evaluation engineering portfolio.

## What it does
- Classification metrics — accuracy, precision, recall, F1, AUC-ROC
- Confusion matrix with error type analysis
- Threshold sensitivity analysis with trade-off visualisation
- ROC curve interpretation
- Regression metrics — MAE, MSE, RMSE, R²
- Predicted vs Actual and residuals visualisation
- Plain-English interpretation of every result

## Dataset
Wisconsin Breast Cancer dataset — two clinical questions:
- Part 1: Is this tumour malignant or benign? (classification)
- Part 2: How large is this tumour? (regression)

## Key results

| Metric | Score |
|--------|-------|
| Classification Accuracy | 0.9825 |
| AUC-ROC | 0.9976 |
| Regression R² | 0.9996 |
| Regression MAE | 0.0456mm |

## Key evaluation findings
1. Classifier missed 2 malignant cases at default threshold 0.5
2. Threshold sensitivity analysis shows lowering to 0.35 recovers
   missed cases at the cost of 1–2 additional false alarms
3. Regression R² of 0.9996 flagged for feature correlation audit
   before production deployment
4. Residuals normally distributed — 95th percentile error 0.14mm

## How to use on your own data
Replace the data loading section with your own:
- y_test — actual labels or values
- y_pred — model predicted labels
- y_prob — model predicted probabilities
All metrics and charts compute automatically.

## Author

Abigael Cherotich — Data Analyst & AI Evaluation Specialist

[LinkedIn](https://www.linkedin.com/in/abigael-cherotich/)
