# Railroad Component Detection for Predictive Maintenance using YOLO

This repository contains a notebook focused on automating the detection of railroad components in images using the YOLO. By accurately labeling and detecting critical components, the project aims to support predictive maintenance efforts—allowing for early identification of potential issues before they escalate.

---

## Technical Overview

The `detection.ipynb` outlines a complete workflow, from data preparation to model training and inference. Here is a high-level technical breakdown:

### 1. Data Preparation

- **Dataset Loading:** `Roboflow` was used to label the images (the original ones can still be found in the `img` directory) which can be downloaded via api directly in the notebook.
- **Preprocessing:** Contrast has been increased to improve model performance, and the images have been resized to 640x640 pixels.

### 2. Model Configuration and Training

- **YOLO:** YOLO v12s was chosen for object detection for its good compromise of training time and overall performance.

### 3. Inference and Visualization

- **Model Inference:** After training, the model is loaded and used to perform object detection on the images in the test and validation sets.
- **Output Generation:** Detected objects are highlighted with bounding boxes, and the resulting annotated images are saved in the `runs/detect` directory.
