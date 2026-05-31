# 🎯 Real-Time Object Detection | YOLOv8 & Ultralytics

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-00FFAB?style=flat-square&logo=yolo&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Ultralytics](https://img.shields.io/badge/Ultralytics-185FA5?style=flat-square)
![Colab](https://img.shields.io/badge/Open%20in%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=black)

> Production-ready object detection pipeline that detects and localizes multiple objects
> in real-world images with confidence scoring and IoU filtering.

---

## 📌 Project Overview

This project deploys a **YOLOv8m** (medium) model using Ultralytics to perform
real-time multi-object detection on images. The pipeline extracts bounding boxes,
class labels, and confidence scores — directly applicable in:

- 🔒 Security surveillance systems
- 🛒 Retail analytics & shelf monitoring
- 🚗 Autonomous vehicle perception
- 🏭 Industrial quality control

---

## 🚀 Pipeline

```
Input Image
    ↓
YOLOv8m Model (pretrained on COCO — 80 classes)
    ↓
Confidence Filtering (conf ≥ 0.2)
    ↓
IoU Filtering (iou = 0.5) — removes duplicate boxes
    ↓
Bounding Box Extraction (xyxy format)
    ↓
Class Label + Probability Scoring
    ↓
Annotated Output Image
```

---

## 📊 Results

| Metric | Value |
|---|---|
| Model | YOLOv8m (medium) |
| Confidence threshold | 0.2 |
| IoU threshold | 0.5 |
| Output format | Bounding boxes (xyxy), class labels, probabilities |
| Deployment status | Production-ready |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| `ultralytics` | YOLOv8 model loading & inference |
| `opencv-python` | Image reading & color conversion |
| `matplotlib` | Visualization of detection results |
| `numpy` | Array operations |
| `pandas` | Data handling |

---

## ▶️ How to Run

1. Open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1GM1u9KW3gAqFvNmqly1Ca-uNR5M5_JDw?usp=sharing)

2. Install dependencies:
```bash
pip install ultralytics
```

3. Upload your image and update the `source` path:
```python
results = model.predict(source="your_image.jpg", save=True, conf=0.2, iou=0.5)
```

4. Run all cells — the annotated output image will be saved and displayed automatically.

---

## 📁 Project Structure

```
yolov8-object-detection/
│
├── notebook.ipynb        # Main detection notebook
├── README.md             # Project documentation
└── sample_output/        # Example detection results
```

---

## 👤 Author

**Mostafa El-Sayed** — Data Scientist | Computer Vision Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/mostafa-nfc)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:m.e.2172000@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MostafaELsayed-217)
