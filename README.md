# carefall
# 🧠 Fall & Crash Detection using YOLOv7 + PyTorch

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-orange.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

> **Real-time Fall & Crash Detection System** powered by **YOLOv7 Keypoint Estimation**, **PyTorch**, and **OpenCV** — featuring **live video processing**, **pose estimation**, and **automated email alerts** on fall/crash detection.

---

## 📸 Overview

This project integrates **computer vision**, **deep learning**, and **automation** to detect **human falls or crashes** in real-time video streams.  
It uses **YOLOv7’s pose/keypoint model** to analyze human postures and triggers an **email alert** if an abnormal event (like a fall) is detected.

The system is designed for:
- 👴 Elderly care & fall prevention  
- 🏍️ Crash detection in smart vehicles  
- 🏠 Smart surveillance & safety systems  

---

## ⚙️ Features

✅ YOLOv7 **keypoint-based human pose detection**  
✅ **Real-time video processing** using OpenCV  
✅ **Automated email alerts** via SMTP  
✅ **Torch model integration** with safe serialization  
✅ **Bounding box + keypoint visualization** on frames  
✅ **Lightweight & modular design** for easy extension  

---

## 🧩 Project Structure

fall_detection_yolov7/
│
├── models/
│ └── yolo.py # YOLOv7 model definition
│
├── utils/
│ ├── datasets.py # Preprocessing (letterbox, dataloaders)
│ ├── general.py # Utility & NMS functions
│ └── plots.py # Visualization helpers
│
├── crash_detection.ipynb # Main notebook for detection logic
├── requirements.txt # Required dependencies
└── README.md # Project documentation

## 🧠 System Workflow

1. **Input Capture**  
   - Uses webcam or video feed (`cv2.VideoCapture`)

2. **Pose Detection**  
   - YOLOv7 keypoint model detects human skeletons

3. **Fall/Crash Classification**  
   - Logic checks angle/orientation of body keypoints

4. **Event Handling**  
   - Saves frame evidence  
   - Sends **email notification** to predefined address  

5. **Visualization**  
   - Displays annotated video output with bounding boxes and keypoints  

---

## 🛠️ Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/fall-detection-yolov7.git
cd fall-detection-yolov7
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Example requirements.txt
torch
torchvision
torchaudio
opencv-python
numpy==1.24.4
matplotlib
tqdm
4️⃣ Verify YOLOv7 Path
Add this to the top of your notebook/script:

import sys, os
sys.path.append(os.path.abspath("C:/Users/aditi/Desktop/fall detection/yolov7"))
🧪 Running the System
▶️ From Jupyter Notebook
Open crash_detection.ipynb and run all cells sequentially.

▶️ From Python Script
Copy code
python crash_detection.py
The system will:

Load the YOLOv7 model

Process video feed

Detect posture anomalies

Send an email alert if a fall/crash is detected

📧 Email Alert Setup
Edit these parameters inside your script:

python
sender = "your_email@gmail.com"
password = "your_app_password"
receiver = "target_email@gmail.com"
⚠️ Important:
If using Gmail, enable 2-Step Verification and create an App Password — regular passwords won’t work.

📊 Example Results
Normal Frame	Fall Detected

🔮 Future Enhancements
📱 Mobile push notifications (Firebase / Twilio)

🎵 Buzzer or voice alerts for local feedback

🚀 Deployment on Raspberry Pi or Jetson Nano

📈 Cloud dashboard for analytics & logs

🤝 Contributing
Contributions, issues, and feature requests are welcome!

Fork the repository

Create your feature branch (git checkout -b feature-name)

Commit changes (git commit -m 'Add new feature')

Push to the branch (git push origin feature-name)

Create a new Pull Request

🧾 License
This project is licensed under the MIT License.
You’re free to use, modify, and distribute this project — just include attribution.

🧩 Acknowledgements
YOLOv7 Repository

PyTorch

OpenCV

NumPy

💡 Author
👩‍💻 Aditi Krishnan
📧 Email: Aditi.g.krishnan@gmail.com
🌐 GitHub: github.com/aditigk1203
