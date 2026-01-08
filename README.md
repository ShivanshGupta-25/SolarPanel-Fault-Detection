# Title : AI-Powered Solar Panel Maintenance & Defect Detection

## Problem Statement:

Build an AI-based system that detects defects, degradation, or maintenance risks in solar panels using 
visual or sensor-derived data. The system must learn from data to identify faults such as cracks, 
hotspots, soiling, or efficiency degradation and produce a final trained AI model exported in ONNX 
format.

Our solution implements an **end-to-end machine learning system** for monitoring and diagnosing solar panel systems using **sensor-based tabular data**.  
A **single ONNX model** performs **four predictive tasks simultaneously**, making it suitable for **real-time, cloud, and edge deployment**.

---

## 📌 Project Motivation

Solar power plants generate large volumes of operational data, but real-world deployment faces challenges:

- Multiple ML models increase deployment complexity  
- Python-based inference is unsuitable for production  
- Edge devices require lightweight, dependency-free models  


## 🧱 Architecture :
- High-level pipeline flow
- Input features
- Preprocessing steps
- Model architecture
- ONNX deployment

Raw Sensor Data  
      ↓  
Data Preprocessing  
(Imputation + Scaling)  
      ↓  
Feature Reduction  
(PCA – Optional)  
      ↓  
Multi-Output Prediction Model  
(Random Forest)  
      ↓  
ONNX Export  
      ↓  
User-Friendly Diagnostic Output  

---

## ✅ Solution
This project:
- Uses **one multi-output ML pipeline**
- Encapsulates preprocessing + model in **ONNX**
- Enables **fast, language-agnostic inference**
--- 

## 🎯 Tasks Covered (Multi-Output Prediction)

1. **Panel Defect Detection** (`panel_defect`)  
2. **Performance Degradation Prediction** (`performance_degradation`)  
3. **Soiling / Hotspot Detection** (`soiling_hotspot`)  
4. **Predictive Maintenance Modeling** (`maintenance_metric`)  

---

## 🧠 Machine Learning Design

- Model: **Random Forest (MultiOutputRegressor)**
- Optimized for **tabular sensor data**
- Fully supported by **ONNX Runtime**

---

## 📊 Model Performance (ONNX Runtime)

```
Panel Defect Accuracy : 93.52%
Performance MAE       : 0.0155
Performance R²        : 0.9887
Soiling MAE           : 0.7660
Soiling R²            : 0.9776
Maintenance MAE       : 0.3899
Maintenance R²        : 0.9963
```

---

## Repository Structure
-----------------------------
```
├── final_model.onnx
├── train.py
├── preprocess.py
├── README.md
├── requirements.txt



--- 

## Technology Used
-----------------------------
- **Python** - Programming Language
- **scikit-learn** - Machine Learning Library
- **pandas** - Data Manipulation Library
- **numpy** - Numerical Library
- **ONNX** - Open Neural Network Exchange
- **ONNX Runtime** - Open Neural Network Runtime
- **skl2onnx** - Converter for scikit-learn models to ONNX's format

---

## Dataset Used
-----------------------------
- Photovoltaic Data Acquisition (PVDAQ) Public Datasets
  - https://data.openei.org/s3_viewer?bucket=oedi-data-lake&prefix=pvdaq%2Fcsv%2F

## 🚀 ONNX Deployment

- Single `.onnx` file
- CPU-only execution
- Edge & cloud compatible

---

## Solar Panel Diagnostic Report
-----------------------------
- Panel Defect Status       : Clean / Moderate / Heavy
- Performance Status        : Normal / Degrading / Severely Degraded
- Soiling / Hotspot Status  : Clean / Moderate / Heavy
- Maintenance Recommendation:
  - No Action Needed
  - Schedule Maintenance
  - Immediate Maintenance Required

--- 

## 🧪 Deployment Readiness
- Single `.onnx` file
- CPU-only execution
- Edge & cloud compatible
- No Python dependencies at ingerence