# Quantum Anomaly Detection Research

## Project Overview

This project examines whether a Quantum model can provide an additional anomaly detection signal alongside CNN and LSTM models.

The work does not aim to prove that Quantum classification is better than classical models based only on overall accuracy.

The main focus is to identify whether the Quantum model can correctly detect actual anomalies that are missed by both CNN and LSTM.

The project is organised into two experimental stages.

---

## Stage 1 — Initial Model Comparison

The first stage established the initial experimental workflow.

CNN, LSTM, and a Quantum Variational Quantum Classifier were evaluated for anomaly detection.

The CTGAN-augmented UNSW-NB15 dataset was used as the experimental dataset.

The initial stage focused on:

- Data preparation
- CNN baseline evaluation
- LSTM baseline evaluation
- Feature reduction
- Quantum model evaluation
- Model prediction comparison
- Initial Quantum-only anomaly analysis

The first-stage results confirmed that CNN and LSTM provide stronger overall prediction performance.

This led to a revised research question:

> Can the Quantum model detect actual anomalies that are missed by both CNN and LSTM?

---

## Stage 2 — Quantum Novelty Validation

The second stage was designed to examine the revised research question using a traceable sample-level comparison.

### Revised Data Setup

The CTGAN-augmented UNSW-NB15 dataset was divided into:

- 40% Training
- 40% Validation
- 20% Testing

A permanent `Sample_ID` was assigned to each record before the dataset split.

The Sample IDs were retained throughout the experiment so that CNN, LSTM, and Quantum predictions could be compared on the same samples.

---

## Model Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| CNN | 98.46% | 82.80% | 96.39% | 89.08% |
| LSTM | 98.23% | 80.63% | 95.90% | 87.61% |
| Quantum | 84.50% | 88.94% | 78.80% | 83.56% |

CNN and LSTM remained stronger in overall model performance.

The Quantum model was therefore evaluated for additional anomaly detection behaviour rather than direct accuracy superiority.

---

## Sample Alignment

CNN, LSTM, and Quantum prediction outputs were aligned using `Sample_ID`.

The final comparison produced:

- Common aligned samples: 2,000
- Actual-label mismatches: 0

This ensured that all three model predictions were compared using the same samples.

---

## Quantum-Only Detection Condition

A true Quantum-only anomaly detection was defined as:

```text
Actual = 1
CNN = 0
LSTM = 0
Quantum = 1
