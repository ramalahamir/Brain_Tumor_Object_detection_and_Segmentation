# 🧠 Brain Tumor Segmentation with YOLOv11 and SAM2
- Author: Ramalah Amir
- Project Type: Medical Image Segmentation (MRI)

## 📌 Overview
This project focuses on the detection and pixel-level segmentation of brain tumors from MRI scans using a combination of:
- YOLOv11 for tumor region detection and classification.
- Segment Anything Model (SAM2) for accurate segmentation masks.
- The goal is to build a fast, reliable, and automated system that supports early diagnosis by medical professionals through precise tumor localization and segmentation.

## 🎯 Objectives
- 🧪 Detect and classify tumors from MRI scans using YOLOv11.
- 🎯 Pass YOLO-predicted bounding boxes to SAM2 for pixel-accurate segmentation.
- 📊 Evaluate model performance using mAP, precision, recall, and accuracy.
- 🏥 Develop a useful tool for real-world medical diagnostics.

## ⚙️ Approach
### 🗂️ Dataset
- MRI brain scans annotated with tumor types: Glioma, Meningioma, Pituitary, and No Tumor.
- Dataset used: Roboflow Tumor Detection Dataset

### 🧠 Model Training
- YOLOv11 trained on the dataset to classify and locate tumors.
- Initially tested with 5 epochs, then increased to 20 epochs for improved accuracy.

### 🧩 Segmentation Pipeline
- YOLOv11 outputs are passed as bounding boxes to SAM2.
- SAM2 generates fine-grained segmentation masks of tumor regions.

### 📈 Evaluation
- Performance analyzed using standard object detection metrics.

# 📂 Code and Usage
- Clone the repository.
- Install dependencies.
- Load trained YOLOv11 model and test images.
- Run YOLO detection
- Pass YOLO output to SAM for segmentation

# 🧪 Results
## 🎯 YOLOv11 Detection Outputs:
![Meningioma](/meningioma_3.jpg)
- Meningioma ✅ Detected
![No Tumor](/no_tumor_1.jpg)
- No Tumor ✅ Detected
![Pituitary](/pituitary_5.jpg)
- Pituitary	✅ Detected
![Glioma](/glioma_2.jpg)
- Glioma ✅ Detected

## 📸 SAM Detection Results:
### 🧠 Segmentation with SAM2:
![Pituitary](/Sam_result_for_pituitary_5.jpg)
- Pituitary ✅ Detected

# 📊 Metrics & Evaluation
- mAP@50–95: ~50% after 20 epochs
- Precision: Improved with YOLO + SAM combo
- Segmentation Accuracy: Visually verified masks show high overlap with true tumor regions

# 🚀 Tools & Libraries
- Python
- YOLOv11 (Ultralytics)
- Segment Anything Model (SAM2)
- Roboflow Dataset
- OpenCV, NumPy, Matplotlib

# 🧾 Credits & References
- Roboflow Brain Tumor Detection Dataset:
- [Dataset: ](https://universe.roboflow.com/brain-tumor-detection-wsera/tumor-detection-ko5jp/dataset/8)
- Meta AI — SAM (Segment Anything Model)
- Ultralytics YOLO
