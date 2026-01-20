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
## 🏗️ System Architecture

The system follows a modular industrial pipeline:

Image acquisition & preprocessing

Data augmentation

CNN-based anomaly detection

Defect severity analysis

Quality grading

Visualization (Grad-CAM)

Batch & real-time inference

API integration

## 🤖 Model Details

Architecture: ResNet-18 (Pretrained on ImageNet)

Training Type: Industrial anomaly detection

Loss Function: Cross-Entropy Loss

Optimizer: Adam

Hardware: NVIDIA T4 GPU (Google Colab)

Only the final classification layer is trained, while the backbone is frozen to avoid overfitting.

## 📊 Defect Severity & Quality Grading

### Defect severity is calculated using image difference analysis.

### Quality Grades
| Severity Range | Quality Grade |
| -------------- | ------------- |
| < 0.05         | ACCEPT        |
| 0.05 – 0.15    | REWORK        |
| > 0.15         | REJECT        |
🎥 Real-Time Inspection

The system supports:

Real-time camera input

Video stream inspection

Frame-by-frame anomaly detection
### Training Loss
![image alt](https://github.com/M-MAHAD1/Bottle-industrial-anomaly-defect-detection/blob/main/Training_Loss_VS_Epochs.PNG)


### Severity Distribution
![Severity Distribution](results/severity_distribution.png)

### Quality Grade Distribution
![Quality Grades](results/quality_grades.png)


This makes it suitable for conveyor belt and production line integration.

## 🌐 API Integration

A Flask-based REST API is provided for seamless industrial integration.
Sample API Output
{
  "label": "DEFECT",
  "severity": 0.13,
  "grade": "REJECT"
}
## 📈 Results & Visualization

Training loss converges close to zero

Grad-CAM highlights defect-relevant regions

Severity-based grading provides actionable insights

Graphs generated:

Training Loss vs Epochs

Defect Severity Distribution

Quality Grade Distribution

## 🚀 Deployment

Can be deployed on-premise or cloud

Supports GPU acceleration

Ready for production with Gunicorn / NGINX

Future optimization using ONNX / TensorRT

### 🧪 How to Run

Clone the repository

git clone https://github.com/your-username/ai-visual-defect-detection.git


Open the notebook in Google Colab

Mount Google Drive and set dataset path

Run cells step by step

### 🔮 Future Work

Full defect segmentation using U-Net / Mask R-CNN

Self-supervised anomaly detection

Edge deployment on industrial cameras

Larger industrial datasets

## 👨‍💻 Author

Muhammad Mahad
Computer Vision & Industrial AI Project
---
