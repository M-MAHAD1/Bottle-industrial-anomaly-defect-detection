# 🏭 AI-Based Visual Defect Detection Tool for Manufacturing

An industrial anomaly detection system using deep learning and computer vision to automatically detect, analyze, and grade surface defects in manufactured products.

This project is implemented using the **MVTec Anomaly Detection – Bottle dataset** and is designed to simulate a **real-world manufacturing quality inspection pipeline**.

---

## 📌 Project Overview

Traditional visual inspection methods in manufacturing are slow, inconsistent, and error-prone.  
This project leverages **AI and deep learning** to build an automated defect detection system that can:

- Detect anomalies in manufactured products
- Estimate defect severity
- Assign quality grades (Accept / Rework / Reject)
- Support batch processing, real-time inspection, and API integration

The system is suitable for **Industry 4.0 and smart manufacturing environments**.

---

## 🧠 Key Features

- Industrial anomaly detection (trained only on good samples)
- CNN-based defect classification using ResNet-18
- Defect severity computation
- Automated quality grading
- Data augmentation for improved generalization
- Grad-CAM based defect visualization
- Batch image inspection
- Real-time camera / video stream support
- REST API using Flask

---

## 📂 Dataset

This project uses the **MVTec Anomaly Detection – Bottle dataset**.

### Dataset Structure
```text
bottle/
 ├── train/
 │    └── good/
 ├── test/
 │    ├── good/
 │    ├── broken_large/
 │    ├── broken_small/
 │    └── contamination/
 └── ground_truth/
      ├── broken_large/
      ├── broken_small/
      └── contamination/
Dataset Characteristics

Training set contains only good images

Defect images appear only during testing

Ground truth masks provided for defective samples

Closely matches real industrial inspection scenarios
---
