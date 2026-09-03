# Construction Site Safety Monitoring Using YOLO11

## Project Overview

This project implements a computer vision system for monitoring construction site safety using YOLO11 object detection.

The model detects workers, personal protective equipment (PPE), safety violations, machinery, vehicles, and safety-related objects.

## Dataset

The dataset was prepared and annotated using Roboflow and exported in YOLO format.

- Total images: 2777
- Training images: 2599
- Validation images: 104
- Test images: 74
- Image size: 640 × 640
- Number of classes: 10

### Classes

1. Hardhat
2. Mask
3. NO-Hardhat
4. NO-Mask
5. NO-Safety Vest
6. Person
7. Safety Cone
8. Safety Vest
9. machinery
10. vehicle

## Model

- Model: YOLO11n
- Training epochs: 30
- Batch size: 16
- Image size: 640 × 640
- GPU: NVIDIA Tesla T4

## Test Results

| Metric | Score |
|---|---:|
| Precision | 82.8% |
| Recall | 63.3% |
| mAP@50 | 69.9% |
| mAP@50-95 | 40.3% |

The model was evaluated on 74 held-out test images containing 760 annotated instances.

## Results

The `results/` directory contains:

- Training results and curves
- Precision-recall curve
- Precision curve
- Recall curve
- F1 curve
- Confusion matrix
- Normalized confusion matrix
- Class distribution
- Numerical training results

## Project Structure

```text
construction_site_safety_yolo11/
│
├── README.md
├── Construction_Site_Safety_YOLO11.ipynb
│
├── config/
│   └── data.yaml
│
└── results/
    ├── README.md
    ├── results.png
    ├── confusion_matrix.png
    ├── confusion_matrix_normalized.png
    ├── BoxPR_curve.png
    ├── BoxP_curve.png
    ├── BoxR_curve.png
    ├── BoxF1_curve.png
    ├── labels.jpg
    └── results.csv
