Hospital Readmission Risk Prediction (Healthcare ML)
📌 Project Overview

Hospital readmission within 30 days is a critical healthcare quality metric. Early readmissions often indicate gaps in treatment effectiveness, discharge planning, or follow-up care and directly impact hospital ratings and patient outcomes.

This project focuses on analyzing real-world hospital admission data and building a machine learning model to identify patients at high risk of readmission within 30 days, with a patient-safety-first approach.

The model is intentionally optimized to prioritize recall over precision, ensuring that high-risk patients are not missed, even if it results in additional false alarms.

📊 Dataset Description

Dataset: Diabetes 130-US hospitals for years 1999–2008

Records: 100,000+ hospital encounters

Scope: Multi-hospital, multi-year clinical dataset

Granularity: Each row represents a single hospital encounter

Key Attributes

Patient demographics

Hospital utilization metrics

Treatment intensity indicators

Clinical complexity indicators

🎯 Problem Statement

Predict whether a patient will be readmitted within 30 days of discharge.

Target Variable Engineering

The original readmitted column was converted into a binary variable:

Value	Meaning
1	Readmitted within 30 days
0	Readmitted after 30 days or not readmitted

This transformation reflects real hospital priorities, where early readmissions are more critical than later admissions.

🧠 Feature Selection

To avoid data leakage and ensure clinical relevance, only meaningful numeric features were retained.

Final Features Used

Age

Time in hospital

Number of lab procedures

Number of procedures

Number of medications

Number of outpatient visits

Number of emergency visits

Number of inpatient visits

Number of diagnoses

Administrative identifiers and outcome-revealing fields were explicitly excluded.

⚙️ Model Selection

Logistic Regression was chosen due to:

Interpretability (important in healthcare)

Probability-based outputs

Suitability for binary classification

Compatibility with threshold tuning

⚖️ Handling Class Imbalance

The dataset was highly imbalanced, with early readmissions forming a minority class.

To address this:

class_weight="balanced" was used

Accuracy was not used as the primary metric

📐 Evaluation Strategy

Given the healthcare context, evaluation focused on:

Recall (Primary Metric)
→ Measures how many high-risk patients are correctly identified

Precision
→ Measures reliability of risk alerts

F1-Score
→ Balances recall and precision

Recall was prioritized because missing a high-risk patient can have serious clinical consequences.

🔧 Threshold Optimization

Instead of using the default 0.5 probability threshold, the Precision–Recall curve was used to tune the decision boundary.

Selected Threshold: ~0.43

Achieved Recall: ~80%

This reflects a safety-first screening model, where false positives are acceptable to minimize missed high-risk cases.

📈 Results Summary

At the chosen threshold:

~80% of early readmissions were successfully identified

False positives increased, but were considered acceptable

The model functions effectively as a risk-screening tool, not a diagnostic system

🏥 Business Impact & Recommendations

The model can be integrated into discharge workflows to flag high-risk patients for:

Follow-up appointments

Medication review

Discharge counseling

Remote monitoring programs

The system is designed to support clinicians, not replace clinical judgment.

⚠️ Limitations & Future Work

Social, behavioral, and post-discharge factors are not included

Dataset reflects historical patterns only

Future improvements may include:

Time-series modeling

Additional clinical features

Two-stage models (ML + clinician review)

✅ Conclusion

This project demonstrates an end-to-end healthcare machine learning pipeline using a large real-world dataset, with a strong emphasis on ethical decision-making, patient safety, and practical deployment considerations.

📁 Folder Structure
project2_healthcare_readmission/
├── notebooks/
│   └── analysis.ipynb
├── visuals/
│   └── precision_recall_curve.png
├── README.md
