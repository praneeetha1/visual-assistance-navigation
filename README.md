# Visual Assistance Navigation (YOLOv8 + Speech)

Real-time object detection and auditory feedback for visually impaired users using YOLOv8 and `pyttsx3`.

---

## Credits

Based on [doguhan2222/object-detection-system-for-the-visually-impaired](https://github.com/doguhan2222/object-detection-system-for-the-visually-impaired).  
Enhanced by [@praneeetha1](https://github.com/praneeetha1) — added live camera input, extended object classes, and continuous speech feedback.

---

## Overview

This system detects and announces nearby objects in real time through speech feedback, estimating distance and direction (left, center, right) to support safer independent navigation.

---

## Key Features

- **YOLOv8-based object detection** (COCO classes)
- **Distance & direction estimation** from bounding boxes
- **Voice alerts** via `pyttsx3`
- **Supports live IP webcam stream or test videos**
- **Keyboard controls:** `p` = pause/resume, `q` = quit

---

## How It Works

1. Capture frames from IP webcam or local video.
2. Run YOLOv8 inference on each frame.
3. Find relevant obstacles and estimate approximate distance.
4. Determine position: left / center / right.
5. Announce the nearest relevant object via speech.

---

## Setup

```bash
git clone https://github.com/praneeetha1/visual-assistance-navigation.git
cd visual-assistance-navigation
python -m venv venv
venv\Scripts\activate   # Windows
pip install -r requirements.txt
python main.py
