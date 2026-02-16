# traffic_monitoring
The project demonstrates object tracking on traffic monitoring and video analytics using YOLO.
# Traffic Congestion Detection using YOLOv8

This project analyzes a traffic video to detect vehicles, estimate their motion speed, and determine congestion levels.  
It uses YOLOv8 tracking to maintain consistent IDs across frames and derives traffic insights from movement behavior.

---

## Overview

The pipeline performs:

1. Vehicle detection and tracking  
2. Per-vehicle speed estimation using frame-to-frame displacement  
3. Slow-vehicle counting  
4. Congestion decision based on density + low speed persistence  
5. Annotated video generation as output  

---

## Tech Stack

- Python  
- OpenCV  
- NumPy  
- Ultralytics YOLOv8  

---

## Vehicle Classes Used

From COCO dataset:
- Car  
- Motorcycle  
- Bus  
- Truck  

---

## How Congestion is Determined

Congestion is flagged when:
- total vehicles exceed a minimum threshold  
- many of them move below a speed limit  
- this situation continues for several frames  

---

## Output

The system produces:
- bounding boxes with track IDs  
- estimated speed for each vehicle  
- vehicle count  
- slow vehicle count  
- traffic state (Free Flow / Moderate / Heavy)  
- congestion alert when triggered  

Output video is saved as:



# Sports Player Tracking with YOLOv8

This project performs basic sports analytics by detecting and tracking players in a match video.  
Each player (person class) receives a persistent ID, and their movement path is visualized across frames.

---

## What the System Does

- Detects players using YOLOv8  
- Tracks them frame-to-frame with unique IDs  
- Draws bounding boxes  
- Plots motion trails  
- Displays live player count  

---

## Tech Stack

- Python  
- OpenCV  
- NumPy  
- Ultralytics YOLOv8  
- Matplotlib / IPython (for notebook display)

---

## Input

A sports video file:

