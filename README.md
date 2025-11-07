# Visual Assistance Navigation (YOLOv8 + Speech)

> Real-time object detection and auditory feedback for visually impaired users using YOLOv8 and `pyttsx3`.

---

## Credits
Based on [doguhan2222/object-detection-system-for-the-visually-impaired](https://github.com/doguhan2222/object-detection-system-for-the-visually-impaired).  
Enhanced by [@praneeetha1](https://github.com/praneeetha1) — added live camera input, extended object classesand continuous speech feedback.

---

## Overview
This system detects and announces nearby objects in real time through speech feedback, estimating distance and direction (left, center, right) to help users navigate safely.

---

## Key Features
- **YOLOv8-based object detection** (80+ classes)  
- **Distance & direction estimation** using bounding boxes  
- **Voice alerts** via `pyttsx3`  
- **Support for live IP webcam or test videos**  
- **Pause (`p`) / Quit (`q`) controls**

---

## 🧩 How It Works
1. Capture live video (`OpenCV` or test videos).  
2. Detect objects with YOLOv8 (`ultralytics`).  
3. Estimate distance using calibrated object width ratios.  
4. Announce results continuously via speech output thread.

---

## Setup
```bash
git clone https://github.com/praneeetha1/visual-assistance-navigation.git
cd visual-assistance-navigation
python -m venv venv
venv\Scripts\activate   # for Windows
pip install -r requirements.txt
python main.py
