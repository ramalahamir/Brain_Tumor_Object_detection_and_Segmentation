# Brain Tumor Segmentation using YOLOv11 and SAM2

## Project Overview
This project aims to detect and segment brain tumors from MRI images.  
We combined **YOLOv11** for detecting tumor regions and **SAM (Segment Anything Model)** for creating accurate segmentation masks.  
The system focuses on identifying three types of tumors: **Glioma**, **Meningioma**, **Pituitary Tumors**, and **No Tumor**.

## Objectives
- Detect tumor regions accurately using YOLOv11.
- Perform pixel-level segmentation using SAM based on detected regions.
- Improve early diagnosis support through fast and automated analysis.
- Evaluate the model using precision, recall, accuracy, and mAP metrics.

## Approach
1. **Data Collection:** MRI images with labeled tumor types.
2. **Preprocessing:** Resized images, organized datasets, created annotations.
3. **YOLOv11 Training:** Trained to detect and classify tumor types.
4. **SAM Segmentation:** Used YOLOv11 outputs to generate pixel-perfect masks.
5. **Evaluation:** Measured performance on test images.

## Results
- Achieved reasonable accuracy and segmentation quality.
- Best mAP (50-95) was around 50% after 20 epochs.
- Improved mask precision by combining detection with segmentation.

## Tools & Libraries
- Python
- YOLOv11
- Segment Anything Model (SAM)
- Ultralytics

## Dataset Used is provided here: 
https://universe.roboflow.com/brain-tumor-detection-wsera/tumor-detection-ko5jp/dataset/8

## How to Run
1. Clone the repository.
2. Install the required libraries and dataset.
3. Load the YOLOv11 trained model.
4. Pass test images and generate masks with SAM.
