# Quantum Anomaly Detection Research

## Project Overview

This project explores a hybrid approach for network intrusion detection by combining classical deep learning models with a quantum machine learning model. The objective is to compare the prediction behavior of CNN, LSTM, and a Variational Quantum Classifier (VQC) using a CTGAN-augmented UNSW-NB15 dataset.

The focus of the project is not only to evaluate prediction accuracy but also to investigate whether the quantum model identifies anomalous samples that are classified differently from the classical models.

---

## Objectives

- Build a complete anomaly detection pipeline.
- Train CNN and LSTM as classical baseline models.
- Train a Quantum Variational Quantum Classifier (VQC).
- Compare prediction results across all models.
- Analyze anomalies uniquely detected by the quantum model.
- Evaluate the practical feasibility of integrating quantum machine learning into an intrusion detection workflow.

---

## Dataset

- Base Dataset: UNSW-NB15
- Data Augmentation: CTGAN
- Preprocessing:
  - Data cleaning
  - Categorical feature encoding
  - Feature scaling
  - Train-test split
  - Principal Component Analysis (PCA)

---

## Project Workflow

```
CTGAN-Augmented UNSW-NB15
            │
            ▼
     Data Preprocessing
            │
            ▼
   Feature Engineering
            │
            ▼
          PCA
            │
            ├──────────► CNN
            │
            ├──────────► LSTM
            │
            └──────────► Quantum VQC
                         │
                         ▼
                Model Comparison
                         │
                         ▼
              Quantum Novelty Analysis
```

---

## Repository Structure

```
Quantum_Anomaly_Detection_Research
│
├── notebooks
├── data
├── models
├── outputs
├── docs
├── requirements.txt
└── README.md
```

---

## Notebooks

| Notebook | Description |
|-----------|-------------|
| 01_Data_Preprocessing | Data preparation and preprocessing |
| 02_CNN_Baseline | CNN model implementation |
| 03_LSTM_Baseline | LSTM model implementation |
| 04_PCA_Feature_Reduction | Feature dimensionality reduction |
| 05_Quantum_VQC | Quantum Variational Quantum Classifier |
| 06_Model_Comparison | Comparison of CNN, LSTM, and Quantum model outputs |

---

## Technologies Used

- Python
- TensorFlow / Keras
- Scikit-learn
- NumPy
- Pandas
- Qiskit
- Qiskit Machine Learning
- IBM Quantum Runtime
- Google Colab

---

## Project Outputs

The project generates:

- Trained CNN model
- Trained LSTM model
- Quantum VQC predictions
- Model comparison results
- Quantum novelty analysis
- Performance evaluation reports

---

## Key Observations

- CNN and LSTM serve as classical baseline models for anomaly detection.
- The Quantum Variational Quantum Classifier is evaluated on a reduced dataset due to current computational limitations.
- The comparison focuses on identifying differences in prediction behavior between classical and quantum models.
- The novelty analysis highlights cases where the quantum model classifies samples differently from the classical models.

---

## Limitations

- Quantum model training is computationally intensive.
- Experiments were performed on a reduced subset of the processed dataset.
- The project is intended as a proof-of-concept for integrating quantum machine learning into an anomaly detection workflow.

---

## Future Work

- Evaluate larger datasets using improved quantum hardware.
- Investigate alternative quantum neural network architectures.
- Explore hybrid classical-quantum ensemble methods.
- Extend the evaluation using additional intrusion detection datasets.

---

## Author

**Bhashyam Sree Darshan**

B.Tech Computer Science and Engineering

Research Area:
- Machine Learning
- Quantum Machine Learning
- Network Security
- Artificial Intelligence

---

## License

This repository is intended for academic and research purposes.
