# Autonomous Cybersecurity: AutoML-Based Intrusion Detection System

## Overview

This project implements a semi-autonomous Intrusion Detection System (IDS) using AutoML-inspired techniques, ensemble learning, and advanced boosting algorithms for cybersecurity applications. The framework is designed to detect malicious network traffic in modern 5G/6G environments while reducing manual machine learning effort.

The system combines multiple tree-based machine learning models with automated feature selection, TVAE-based data balancing, and confidence-based ensemble stacking to improve attack detection performance and robustness.

---

# Research Inspiration

This project is inspired by the research paper:

**"Towards Autonomous Cybersecurity: An Intelligent AutoML Framework for Autonomous Intrusion Detection"**

Paper Link:
https://arxiv.org/abs/2409.03141

The project adapts and explains the concepts presented in the paper, including:

* AutoML-based intrusion detection
* Automated feature selection
* Ensemble learning
* TVAE-based balancing
* Autonomous cybersecurity workflows for 5G/6G environments

The implementation provided in this repository is intended for educational, research, and learning purposes.


---

# Features

* AutoML-inspired IDS pipeline
* Automated Feature Selection (AutoFE/AutoFS)
* TVAE-based synthetic attack generation
* Ensemble Learning and Confidence-Based Stacking
* Multiple Boosting Algorithms
* Designed for 5G/6G Cybersecurity Environments
* Handles Imbalanced Network Traffic Data

---

# Machine Learning Models Used

The framework trains and evaluates the following tree-based models:

* Decision Tree (DT)
* Random Forest (RF)
* Extra Trees (ET)
* XGBoost
* LightGBM
* CatBoost

These models are compared based on:

* Accuracy
* Precision
* Recall
* F1-Score
* Cross Validation Performance

---

# Datasets Used

## CICIDS2017

Contains realistic benign and malicious traffic including:

* DDoS
* PortScan
* Brute Force
* Botnet
* Web Attacks

## 5G-NIDD

Modern intrusion detection dataset designed for:

* 5G networks
* IoT communication
* Next-generation cybersecurity environments

---

# Important Features Used

The IDS uses network flow-based features such as:

* Flow Duration
* Flow Bytes/s
* Flow Packets/s
* Packet Length Mean
* SYN Flag Count
* ACK Flag Count
* Inter Arrival Time (IAT)
* Active Mean / Idle Mean

---

# Workflow

```text
Dataset Loading
        ↓
Data Preprocessing
        ↓
Train 6 Base Tree Models
        ↓
Model Evaluation
        ↓
Automated Feature Selection
        ↓
TVAE Data Balancing
        ↓
Retrain Optimized Models
        ↓
Ensemble Learning & Stacking
        ↓
Final Intrusion Detection System
```

---

# Automated Feature Selection

Feature importance values are extracted from all six tree models.

The framework:

1. Computes feature importance for each model
2. Averages importance scores
3. Sorts features by cumulative importance
4. Selects features contributing to 90% importance

This helps:

* reduce dimensionality
* improve training speed
* reduce overfitting
* keep only important cybersecurity indicators

---

# TVAE-Based Balancing

Cybersecurity datasets are highly imbalanced because attack traffic is much smaller than benign traffic.

The project uses:

## TVAE (Tabular Variational Autoencoder)

TVAE:

* learns attack data distributions
* generates synthetic minority attack samples
* improves rare attack detection

---

# Ensemble Learning

The framework combines predictions from top-performing models using:

* Stacking
* Confidence-Based Ensemble Learning

This improves:

* robustness
* generalization
* attack detection accuracy

---

# Technologies Used

* Python
* Scikit-learn
* XGBoost
* LightGBM
* CatBoost
* Pandas
* NumPy
* SDV / TVAE
* Matplotlib

---

# Project Contributions

* Semi-autonomous cybersecurity framework
* Automated feature selection pipeline
* TVAE-based attack balancing
* Confidence-based ensemble stacking
* AutoML-inspired IDS workflow

---

# Future Improvements

* Real-time intrusion detection
* Live packet capture integration
* Deep learning-based IDS
* Explainable AI for cybersecurity
* Federated intrusion detection systems

---

# Conclusion

This project demonstrates how AutoML concepts can be integrated into cybersecurity systems to create scalable and intelligent intrusion detection frameworks. By combining boosting algorithms, automated feature selection, TVAE balancing, and ensemble learning, the framework achieves robust intrusion detection performance suitable for future autonomous network environments.
