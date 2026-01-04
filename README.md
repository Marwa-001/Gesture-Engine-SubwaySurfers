# Gesture-Engine-SubwaySurfers 🕹️⚡

A high-performance, low-latency gesture control engine for Subway Surfers built with Python, MediaPipe, and OpenCV.

Most gesture-controlled projects are cool for a demo but physically exhausting for actual gameplay. This project solves the **"Fatigue Problem"** by replacing wide arm movements with a high-precision, micro-gesture system.

## 🚀 Key Innovation: The "Static Wrist" Logic

Instead of tracking the hand's X/Y position across the frame—which leads to jitter and shoulder strain—this engine treats the hand as a **3-way physical toggle switch**.

* **Vector-Angle Steering:** The script calculates the vector angle between the **Wrist (Landmark 0)** and the **Palm Center (Landmark 9)**. A subtle 15° pivot is all that's required to switch lanes.
* **Ergonomics:** Your wrist remains relatively static, allowing for long-term play without the "gym workout" usually associated with Computer Vision apps.



## ✨ Features

* **Zero-Latency Execution:** Stripped `pyautogui` default delays to 0ms and optimized frame processing to $640 \times 480$.
* **State-Based Control:** Unlike "flick" detection, lanes are mapped to physical hand states, ensuring robust stability.
* **Gesture Mapping:**
    * 🖐️ **Tilt Left/Right:** Lane Navigation
    * ☝️ **Index Extended:** Jump
    * ✊ **Clenched Fist:** Roll
* **Visual HUD:** Real-time tilt indicator and "Neutral Zone" feedback provided on-screen.



## 🛠️ Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Gesture-Engine-SubwaySurfers.git](https://github.com/YOUR_USERNAME/Gesture-Engine-SubwaySurfers.git)
   cd Gesture-Engine-SubwaySurfers
   
Install dependencies:
pip install -r requirements.txt

🎮 How to Play
Open Subway Surfers: Launch the game via a web browser or an Android emulator.

Run the script: ```bash python main.py

Calibrate: Position your hand in the center of the webcam feed until the HUD indicates a "Neutral" state.

Controls:

Tilt: Pivot your palm left or right to switch lanes.

Jump/Roll: Use the mapped finger gestures to navigate obstacles in real-time.
