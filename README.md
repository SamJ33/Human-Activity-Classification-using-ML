# Human-Activity-Classification-using-ML
This project aims to help understand human activity and classify it in real time according to sensory data


[![Python](https://img.shields.io/badge/python-3.11-blue)](https://www.python.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)  
[![UCI Dataset](https://img.shields.io/badge/Dataset-UCI-blueviolet)](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)

---

## Overview
**Human Activity Classification (HAC)** is a system that classifies human activities using smartphone sensor data, including accelerometer and gyroscope readings.
The system predicts activities with high accuracy, achieving **97.4% overall classification accuracy** on the UCI dataset.


Instead of the original UCI activity labels, activities have been **remapped into three intensity levels** for activity intensity tracking:  

- **Low Activity**  
- **Medium Activity**  
- **High Activity**  

This remapping enables applications focused on **activity intensity monitoring**, **health tracking**, and **wearable devices**.

---

## Dataset
- Data source: **[UCI Human Activity Recognition Using Smartphones Dataset](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)**  
- Sensors: Accelerometer and Gyroscope along x, y, and z axes  
- Features: Time-domain and frequency-domain metrics extracted from raw signals  
- Original UCI Activity Labels:  
  - Walking  
  - Walking_Upstairs  
  - Walking_Downstairs  
  - Sitting  
  - Standing  
  - Laying  
- Remapped Activity Intensity Labels:  
  - Low Activity  
  - Medium Activity  
  - High Activity  

---

## Features
- Real-time and batch classification of activity intensity  
- Preprocessing: Noise removal, feature extraction, and scaling  
- Supports multiple classifier options (Random Forest, AdaBoost)  
- Scalable to additional sensor inputs or activity classes  

---
## Exploratory Data Analysis (EDA)
- **Correlation Heatmaps**: Visualize relationships between features
- **Feature Importance**: Using Random Forests to identify impactful metrics
- **Standard Scaling**: Normalize features for better model performance
---
## Model
- **Preprocessing**: Noise removal, feature extraction, scaling
- **Classifier**: Random Forest and AdaBoost
- **Activity Labels**:
- **Original UCI Labels**: Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing, Laying
- **Remapped Intensity Labels**: Low, Medium, High
---
## Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/human-activity-classification.git
cd human-activity-classification

# Create a virtual environment
python -m venv venv
source venv/bin/activate      # Linux/Mac
venv\Scripts\activate         # Windows

# Install dependencies
pip install -r requirements.txt

##  Usage
# Train the Model
python scripts/train.py --data_path data/UCI_HAR_dataset.csv
Trains the classifier and saves the model in models/.

# Make Predictions
python scripts/predict.py --model_path models/hac_model.pth --input_data data/test_data.csv
