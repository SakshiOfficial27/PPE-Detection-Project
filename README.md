# 🦺 PPE Detection System using YOLOv8

<div align="center">

**A real-time AI-powered workplace safety monitoring system that detects PPE compliance using YOLOv8 and Computer Vision.**

</div>

---

## 📌 Project Overview

The **PPE Detection System** is a real-time safety monitoring application built with Artificial Intelligence and Computer Vision. It automatically detects whether workers are wearing required Personal Protective Equipment (PPE) — including helmets, gloves, masks, safety vests, and goggles — through live video feeds.

By replacing manual inspection with automated AI monitoring, this system significantly improves workplace safety and reduces human error in safety compliance tracking.

---

## 🚀 Features

- ✅ **Real-time PPE detection** using YOLOv8
- ✅ **Multi-object detection** — detects multiple PPE items simultaneously
- ✅ **Live video & image** detection support
- ✅ **Confidence score display** for each detected object
- ✅ **MySQL database integration** for storing detection logs
- ✅ **Fast and accurate** object detection
- ✅ **Flask-based web backend** for easy deployment
- ✅ **User-friendly** safety monitoring interface

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| YOLOv8 (Ultralytics) | Object detection model |
| OpenCV | Video frame processing |
| Flask | Web application backend |
| MySQL | Detection data storage |
| Roboflow | Dataset sourcing & annotation |

---

## 📂 Project Structure

```
FlaskTutorial_YOLOv8_Web/
├── static/               # Static assets (CSS, JS, images)
├── templates/            # HTML templates for Flask
├── YOLO-Weights/         # Trained YOLOv8 model weights
├── build/                # Build output
├── dist/                 # Distribution files
├── flaskapp.py           # Main Flask application
├── YOLO_Video.py         # Video detection logic
├── flaskapp.spec         # PyInstaller spec file
├── requirements.txt      # Python dependencies
└── Dockerfile            # Docker configuration
```

---

## 📂 Project Modules

1. **Dataset Collection** — Gathering PPE images from Roboflow
2. **Data Annotation** — Labeling PPE objects in images
3. **Model Training** — Training YOLOv8 on the PPE dataset
4. **Real-time Detection** — Live video frame inference
5. **Database Integration** — Logging detections to MySQL
6. **Result Monitoring** — Displaying detection output via Flask

---

## 🤖 YOLOv8 Model

This project uses **YOLOv8 (You Only Look Once — Version 8)** by Ultralytics for object detection, chosen for its outstanding performance in real-time scenarios with high speed and accuracy.

---

## 📊 Dataset Information

| Property | Details |
|---|---|
| Dataset Source | Roboflow |
| Total Images | 1000+ |
| Total Classes | 10 PPE Classes |

### 🏷️ PPE Classes

| # | Class | # | Class |
|---|---|---|---|
| 1 | Helmet | 6 | Boots |
| 2 | Safety Vest | 7 | Person |
| 3 | Gloves | 8 | PPE Kit |
| 4 | Goggles | 9 | No Helmet |
| 5 | Face Mask | 10 | No Vest |

---

## 💻 Core Libraries

```python
from ultralytics import YOLO
import cv2
import mysql.connector
from flask import Flask
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/SakshiOfficial27/PPE-Detection-Project.git
cd ppe-detection-system
```

### 2️⃣ Install Required Libraries

```bash
pip install ultralytics
pip install opencv-python
pip install flask
pip install mysql-connector-python
```

Or install all at once:

```bash
pip install -r requirements.txt
```

### 3️⃣ Configure MySQL Database

Set up your MySQL database and update the connection credentials in `flaskapp.py`.

### 4️⃣ Run the Application

```bash
python flaskapp.py
```

Open your browser and visit: `http://localhost:5000`

---

## 🐳 Run with Docker (Optional)

```bash
docker build -t ppe-detection .
docker run -p 5000:5000 ppe-detection
```

---

## 📸 How It Works

```
📷 Camera Input
      ↓
🖼️  Frame Captured by OpenCV
      ↓
🤖 YOLOv8 Processes Each Frame
      ↓
🦺 PPE Objects Detected in Real-Time
      ↓
📊 Confidence Score Displayed on Screen
      ↓
🗄️  Detection Data Saved to MySQL
```

---

## 🗄️ Database Schema

MySQL database stores the following for each detection event:

| Field | Description |
|---|---|
| `object_class` | Detected PPE class name |
| `confidence_score` | Detection confidence percentage |
| `timestamp` | Date and time of detection |
| `detection_id` | Unique record identifier |

---

## 🎯 Advantages

- 🔒 Improves workplace safety & compliance
- 🤖 Reduces need for manual monitoring
- ⚡ Fast and accurate real-time detection
- 📁 Automated logging and record-keeping
- 🖥️ Easy to deploy and use

---

## 📍 Applications

- 🏗️ Construction Sites
- 🏭 Factories & Manufacturing Plants
- 📦 Warehouses
- 🔬 Laboratories
- ⚙️ Industrial & Hazardous Work Areas

---

## 📈 Future Enhancements

- [ ] 📧 Email alert system for PPE violations
- [ ] 📱 Mobile application integration
- [ ] 🧾 Automated attendance monitoring
- [ ] ☁️ Cloud database support
- [ ] 🔍 Face recognition integration
- [ ] 📊 Analytics dashboard for safety reports

---

## 👩‍💻 Author

**Sakshi Chavhan**

LinkedIn: https://www.linkedin.com/in/sakshi40765/
GitHub: https://github.com/SakshiOfficial27
Email: chavhansakshi14@gmail.com


---

## 📄 License

This project is developed for **educational and research purposes**.

---

<div align="center">
  <i>⭐ If you found this project helpful, please give it a star!</i>
</div>
