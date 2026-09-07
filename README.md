# Intern Performance Prediction

**Internee.pk — Data Analyst Domain — Task 3**

## Objective
Predict intern performance based on engagement and task completion signals, and provide mentors with actionable insights for personalized guidance.

## What this project does
- Builds a dataset covering attendance, task submission rate, feedback score, and mentor interactions (synthetic — see Data note)
- Trains a Random Forest classifier (scikit-learn) to predict each intern's probability of success
- Flags interns as "High Risk," "Watch List," or "On Track" to help mentors prioritize outreach

## Data note
No real dataset was provided, so `intern_performance_data.csv` was generated synthetically (500 interns, fixed random seed) using the fields specified in the task brief.

## Files
| File | Description |
|---|---|
| `intern_performance_data.csv` | Generated dataset |
| `intern_performance_predictions.csv` | Per-intern success probability + risk flag |
| `confusion_matrix.png` | Model evaluation |
| `feature_importance.png` | What drives predicted success |

## Key findings
- **Accuracy:** 73% on test data
- **Top predictors:** attendance rate (33%) and submission rate (30%) — together drive over 60% of the model's decisions
- Feedback score and mentor interactions matter less than simply showing up and submitting work
- **Recommendation:** mentors should use the `risk_flag` column in the predictions file to prioritize check-ins for "High Risk" and "Watch List" interns

## Tools
Python (pandas, numpy, scikit-learn, matplotlib) in Google Colab.

## Author
Muhammad Ahmad — Data Analyst Intern, Internee.pk
