# Autonomous-Laser-Weeder
An autonomous AI-powered robot that uses YOLOv8 and an ESP32-CAM to detect and target weeds with a laser gimbal .An end-to-end robotics project that uses machine learning to identify weeds among crops and targets them in real-time using a 2-axis laser gimbal.
<br>
Author - Meet Nagariya

![Project Demo Image/GIF](link_to_your_image_here) *(Note: Replace this with a photo of your hardware or a GIF of the laser aiming!)*

## 🚀 Project Overview
This project bridges computer vision and physical hardware to create a targeted weed-control system. An ESP32-CAM streams overhead video to a local machine, where a custom-trained YOLOv8 Nano model differentiates between crops and weeds. The coordinates of the detected weeds are mapped to pan-tilt angles and sent back to the microcontroller to aim a laser diode.

## 🛠️ System Architecture
1. **Perception:** ESP32-CAM module streams live video over WiFi.
2. **Inference:** Python script runs locally, processing frames through a YOLOv8 object detection model trained on a custom two-class dataset (Crop vs. Weed).
3. **Control:** Bounding box coordinates are converted into kinematic angles for the pan-tilt servo mechanism.
4. **Actuation:** ESP32 translates angles into PWM signals to drive the servos and trigger the laser.

## 🗂️ Repository Structure
* `/ai_model`: Jupyter notebooks/Python scripts for YOLOv8 training and validation.
* `/esp32_firmware`: C++ code for camera streaming and servo/laser control.
* `/laptop_inference`: Python scripts for real-time video processing and serial/WiFi communication.
* `/hardware`: Wiring diagrams and component lists.

## ⚙️ Hardware Used
* ESP32-CAM Module
* 2x Micro Servos (Pan/Tilt Mechanism)
* 5V Laser Diode
* Custom mounting hardware

## 🚀 How to Run (Coming Soon)
*Instructions on how to flash the ESP32, set up the Python environment, and run the inference script will be added as the project progresses.*
