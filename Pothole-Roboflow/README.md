# My-Projects
# 🕳️ Pothole Detection using Roboflow3.0 (Instance Segmentation)

This project uses **Roboflow 3.0 segmentation model** to detect potholes in images and videos. It outputs both **bounding boxes** and **pixel-perfect shape outlines**, making it suitable for road condition monitoring and automated maintenance detection.

---
#cd Features

- 📦 Roboflow 3.0 instance segmentation model (`COCOn-seg`)
- ✅ Detects potholes with bounding boxes and segmentation masks
- 🖼️ Supports image and video inference
- 🎨 Visualizes contours and filled masks using OpenCV
- 🔁 Real-time video processing with annotated output
- 📈 Performance metrics (mAP, precision, recall)

---
# Tools:
- python 3.9.6
- jupyter Notebook(vscode)
- pytorch
- numpy
- matplotlib

---
# Steps:
1. Created dataset by collecting related images and labeling them accordingly and splitting the dataset(Train, validation, test) in Roboflow:
2. Trained the model using Roboflow 3.0 instance segementaion with checkpoint "COCOn-seg", image_size: 1024*1024
3. Evaluate on the test set
4. Deployed model using "Hosted image inference" for image testing and "Hosted video inference" for video testing

---
# weights
- model is trained for 300 epochs straight


---
# Metrics
Metric
Value
What It Means
mAP@50
85.1%
Your model detects potholes correctly 85.1% of the time at IoU ≥ 0.5.
Precision
87.7%
Of all the detections your model made, 87.7% were correct (true positives).
Recall
76.0%
Of all actual potholes, your model correctly identified 76% of them.

---
# Summary
- High Precision, Lower Recall: model is very accurate when it makes a detection but misses some potholes (false negatives).
- mAP@50 of 85.1%: That’s a strong indicator of model performance. Above 80% is typically considered good for object detection tasks.

---
# Acknowledgements
- Ultralytics YOLOv8: https://github.com/ultralytics/ultralytics
- Roboflow: https://roboflow.com
- OpenCV: https://opencv.org/
- Supervision: https://github.com/roboflow/supervision