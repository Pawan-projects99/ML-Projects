# My-Projects
# 🕳️ Pothole Detection using YOLOv8 (Instance Segmentation)

This project uses **YOLOv8's segmentation model** to detect potholes in images and videos. It outputs both **bounding boxes** and **pixel-perfect shape outlines**, making it suitable for road condition monitoring and automated maintenance detection.

---
#cd Features

- 📦 YOLOv8 instance segmentation model (`yolov8m-seg`)
- ✅ Detects potholes with bounding boxes and segmentation masks
- 🖼️ Supports image and video inference
- 🎨 Visualizes contours and filled masks using OpenCV
- 🔁 Real-time video processing with annotated output
- 📈 Performance metrics (mAP, precision, recall)

---
# Tools:
- python 3.13.5
- jupyter Notebook(vscode)
- Google colab (for training)(t4-GPU)
- pytorch
- numpy
- matplotlib

---
# Steps:
1. Download dataset from Roboflow:

rf = Roboflow(api_key="YOUR_API_KEY")
project = rf.workspace().project("pothole-segmentation")
dataset = project.version(3).download("yolov8")

2. Train the model
3. Evaluate on the test set
4. Run inference on a sample image and video

---
# weights
- model is trained for both 100 Epochs and 200 Epochs
- Checkpoints for both are included in the .zip format inthe project

---
# Metrics
Metric
Meaning
Images
Number of images used in the test set (55)
Instances
Total number of object instances (potholes) annotated (193)
Box(P)
Precision for bounding boxes → 84% of detections were correct
Box(R)
Recall for bounding boxes → 62.7% of actual potholes were found
mAP50
Mean Average Precision at IoU=0.5 for boxes → good indicator (73.4%)
mAP50-95
Average over IoU thresholds 0.5 to 0.95 (harder metric) → 61.8%
Mask(P)
Precision for segmentation masks → 84%
Mask(R)
Recall for segmentation masks → 62.7%
Mask mAP50
Segmentation precision at IoU=0.5 → 73.7%
Mask mAP50-95
Stricter average for mask IoU from 0.5 to 0.95 → 56.4%

---
# Summary
- High precision (0.84): when the model detects something, it’s usually correct.
- Moderate recall (0.627): it misses some potholes.
- Mask mAP50 is strong (0.737), showing the segmentation masks are good at standard IoU.

---
# Acknowledgements
- Ultralytics YOLOv8: https://github.com/ultralytics/ultralytics
- Roboflow: https://roboflow.com
- OpenCV: https://opencv.org/