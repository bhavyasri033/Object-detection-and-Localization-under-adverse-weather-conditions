# 🌧️ Object Classification and Localization under Adverse Weather Conditions

##  Overview

This project investigates the robustness of YOLOv8-based object detection models under adverse weather conditions such as fog, rain, snow, and low-light environments.

Instead of proposing a new architecture, this work focuses on:

- Evaluating baseline YOLOv8 performance
- Analyzing environmental domain shift
- Fine-tuning the model on weather-degraded data
- Comparing robustness improvements

The goal is to understand how environmental degradation impacts object **classification** and **localization** in autonomous driving scenarios.

---

##  Problem Statement

Object detection models trained on clear-weather datasets often fail to generalize under adverse weather conditions. Environmental degradations:

- Reduce contrast (Fog)
- Introduce streak artifacts (Rain)
- Distort textures (Snow)
- Reduce illumination (Night)

These effects lead to:

- Increased false negatives
- Localization instability
- Reduced confidence scores
- Performance degradation in safety-critical systems

---

##  Dataset

**Dataset Used:** ACDC (Adverse Conditions Dataset with Correspondences)

### Weather Categories
- Fog
- Rain
- Snow
- Night

### Object Classes
- Person
- Bicycle
- Car
- Motor
- Bus
- Train

### Dataset Statistics
- Total Images: 5000
- Multi-weather distribution
- Bounding-box annotations
- Real-world urban driving scenes

---

##  Model Architecture

Model Used: **YOLOv8n (Pre-trained)**

Key Characteristics:
- Single-stage detector
- Real-time inference capability
- Pre-trained on clear-weather dataset
- Fine-tuned on adverse weather samples

---

## ⚙️ Methodology

### 1️⃣ Baseline Evaluation
- Evaluated pre-trained YOLOv8n
- Tested under Fog, Rain, Snow, and Night
- Metrics: Precision, Recall, mAP@50, mAP@50–95

### 2️⃣ Fine-Tuning
- Epochs: 25
- Batch Size: 16
- Input Resolution: 640×640
- Optimizer: AdamW
- First 10 layers frozen
- Weather-aware augmentation applied

### 3️⃣ Comparative Analysis
- Baseline vs Fine-Tuned comparison
- Class-wise performance analysis
- Localization gap analysis (mAP@50 vs mAP@50–95)
<img width="463" height="553" alt="image" src="https://github.com/user-attachments/assets/970c2ba1-8719-46f8-8371-92746b426a76" />

---

Key Observations:
- Fine-tuning improves robustness across all weather conditions
- Small objects show significant improvement
- Localization stability improves under stricter IoU thresholds
- Extreme degradation remains challenging

---

##  Evaluation Metrics

- Precision
- Recall
- mAP@50
- mAP@50–95
- IoU (Intersection over Union)

---

##  Future Work

- Multi-dataset training for improved generalization
- Domain adaptation techniques
- Integration with image enhancement modules
- Real-world edge deployment validation
- Multi-modal sensor fusion (LiDAR + Camera)

---

##  Author

**Bhavya Sri Chapalamadugu**  
B.Tech – Computer Science Engineering (AI & ML)  
Project: Object Classification and Localization under Adverse Weather Conditions  

---

##  License

This project is developed for academic and research purposes.
