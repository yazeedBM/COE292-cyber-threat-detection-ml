Cyber Threat Detection using Machine Learning
Project Overview

This project focuses on detecting cyber threats in network traffic using Machine Learning techniques. The dataset includes both normal and malicious traffic, with attack types such as:

DDoS

Brute Force

Ransomware

Normal traffic

The objective is to build classification models capable of identifying and categorizing network traffic to enhance intrusion detection systems (IDS).

This project was developed for:

COE 292 – Introduction to Artificial Intelligence
King Fahd University of Petroleum & Minerals

Dataset Information

Total samples: 1430

Total features: 21 (excluding Timestamp and Label)

Classes: 4 (DDoS, Ransomware, Brute Force, Normal)

Dataset balance: Balanced (~25% per class)

Source:
https://www.kaggle.com/datasets/hussainsheikh03/cyber-threat-detection

Problem Type

Multi-class classification problem:

Predicting Attack_Type based on network traffic metadata.

The dataset also includes:

Label → Binary classification (0 = Normal, 1 = Malicious)

Attack_Type → Specific attack category

🔎 Features Used

Key network features include:

Protocol (TCP, UDP, ICMP)

Packet Length

Duration

Source Port

Destination Port

Bytes Sent

Bytes Received

TCP Flags

Flow Packets per second

Flow Bytes per second

These features represent traffic behavior and are commonly used in intrusion detection systems.

Data Preprocessing

The following preprocessing steps were applied:

Removed non-informative columns (Timestamp, IP addresses)

Handled missing values

One-hot encoded categorical features (Protocol, Flags)

Encoded target labels

Stratified train-test split

Feature scaling (for KNN, SVM, DNN models)

Models Implemented

The following machine learning models were tested:

K-Nearest Neighbors (KNN)

Random Forest

Deep Neural Network (DNN)

Random Forest showed strong performance due to its ability to handle structured tabular data effectively.

Evaluation Metrics

Models were evaluated using:

Accuracy

Confusion Matrix

Precision

Recall

F1-score

Visualizations

Exploratory Data Analysis (EDA) included:

Class distribution plots

Scatter plots (Flow rates, Bytes sent/received)

Violin plots

Feature distribution histograms

These visualizations helped analyze feature separation and class overlap.

Conclusion

Cyber threat classification plays a critical role in enhancing cybersecurity systems. Accurate detection enables:

Real-time threat mitigation

Prevention of data breaches

Reduced financial loss

Improved network integrity

While binary classification (Malicious vs Normal) shows strong separability, multi-class classification remains more challenging due to overlapping feature distributions between attack types.
