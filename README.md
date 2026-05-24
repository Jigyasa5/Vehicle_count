# Vehicle_count Project 
## Project Overview
This project focuses on real time vehicle detection using the YOLO object detection model. The system is trained to detect four vehicle categories: bus, car, motorbike, and truck. The project was developed and trained using Python OpenCV, and YOLO framework. The main objective of the project is to accurately detect vehicles from images for applications such as traffic monitoring, smart transportation systems, and automated vehicle analysis.

## Dataset Used
The dataset used for this project is a custom vehicle detection dataset obtained from Roboflow(Link: https://universe.roboflow.com/skripsi-1qzlz/vehicle-detection-bvxpr/dataset/1). It contains labeled images of different vehicles in YOLO format. The dataset includes four classes:
-Bus
-Car
-Motorbike
-Truck

## Dataset Structure
```text
Vehicle_count/
├── train/
│   ├── images/
│   └── labels/
├── valid/
│   ├── images/
│   └── labels/
├── test/
│   ├── images/
│   └── labels/
└── data.yaml
```

---
# Technologies Used
- Python
- YOLO
- OpenCV
- NumPy
- Matplotlib

---
# Data Preprocessing
The following preprocessing steps were performed before training:
- Image resizing to 640×640
- Data normalization
- Annotation validation
- Dataset splitting into train, validation, and test sets
- YOLO label format verification
- Path configuration in `data.yaml`

---
# Model Performance

| Metric | Score |
|---|---|
| mAP50 | 93.71% |
| mAP50-95 | 75.34% |
| Precision | 90.89% |
| Recall | 88.73% |

The model achieved strong object detection performance with high precision and recall values.

# Architecture Explanation

YOLOv8 is a one-stage object detection architecture designed for fast and accurate real-time detection.

## Architecture Components

### Backbone
Extracts important image features.

### Neck
Combines features from different scales.

### Detection Head
Predicts:
- Bounding boxes
- Object classes
- Confidence scores

This architecture enables simultaneous object localization and classification.

---

# Challenges Faced
- Managing dataset paths in Google Colab
- Handling annotation formatting issues
- Avoiding overfitting
- Reducing false detections in crowded scenes
- Limited GPU resources in Colab

---
# Sample Outputs
The project generates:
- Vehicle detection outputs
![Detection Output](output1.png)
![Detection Output](output2.png)
- Confusion matrix
- Precision-Recall curves
- Training graphs
