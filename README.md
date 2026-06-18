# 🌫️ AlertVision – AI-Powered Image & Video Dehazing System

🚀 *Restoring clarity, enhancing visibility, and transforming hazy visuals through the power of AI.*

## 📌 Overview

AlertVision is an AI-powered image and video dehazing application designed to improve visibility in foggy, hazy, and low-contrast environments. The system combines advanced deep learning techniques with traditional computer vision methods to restore image clarity and enhance visual quality.

Built with a modern React frontend and a Python Flask backend, AlertVision allows users to upload images or videos through an intuitive web interface and receive enhanced outputs generated using PyTorch and OpenCV-based processing pipelines.

---

## ✨ Key Features

* 🌫️ Remove haze and fog from images and videos
* 🤖 Deep learning-based image restoration
* 🎯 Traditional Dark Channel Prior dehazing support
* 📤 Drag-and-drop media upload interface
* ⚡ Fast and responsive React frontend
* 🔄 Real-time frontend-backend communication
* 📊 Improved visibility and image quality
* 🖥️ User-friendly and modern interface

---

## 🏗️ System Architecture

```text
Frontend (React + Vite)
        ↓
Axios API Request
        ↓
Flask Backend
        ↓
PyTorch Model + OpenCV Processing
        ↓
Enhanced Output Generated
        ↓
Frontend Displays Result
```

---

## 🛠️ Technologies Used

### Frontend

* React
* TypeScript
* Vite
* Tailwind CSS
* Axios
* React Dropzone

### Backend

* Python
* Flask
* Flask-CORS
* PyTorch
* OpenCV
* NumPy
* Pillow (PIL)
* Matplotlib

---

## 🤖 AI & Computer Vision Techniques

### Dark Channel Prior (Traditional Method)

A classical image dehazing algorithm based on atmospheric scattering principles.

**Advantages**

* No model training required
* Lightweight implementation
* Traditional computer vision approach
* Effective for many haze conditions

### Feature Fusion Attention Network (Deep Learning)

A CNN-based deep learning model that learns haze removal patterns directly from training data.

**Key Concepts**

* Convolutional Neural Networks (CNN)
* Feature Extraction
* Attention Mechanisms
* Deep Learning Inference
* Image Restoration

---

## 🔄 How It Works

1. User uploads a hazy image or video.
2. The React frontend sends the file to the Flask backend using an HTTP POST request.
3. OpenCV and PIL preprocess the uploaded media.
4. PyTorch loads the trained dehazing model and performs inference.
5. The enhanced output is generated.
6. The processed image or video is returned to the frontend.
7. The user can instantly view the dehazed result.

---

## 💡 Concepts Demonstrated

* Full-Stack Development
* Computer Vision
* Deep Learning
* Image Processing
* REST API Integration
* Frontend-Backend Communication
* Model Inference
* File Handling
* Image Enhancement
* AI-Powered Media Processing

---

## 🎯 Challenges Solved

* Python virtual environment setup
* Frontend-backend integration
* Dependency and compatibility issues
* PyTorch model loading
* REST API communication
* File upload and processing workflows
* Debugging and deployment configuration

---

## ⚠️ Limitations

* Processing speed depends on hardware resources.
* Large videos require longer inference time.
* CPU execution is slower than GPU acceleration.
* Performance depends on the quality of the trained model.

---

## 🔮 Future Enhancements

* 🎤 Real-time webcam dehazing
* ⚡ GPU acceleration support
* ☁️ Cloud deployment
* 🧠 Improved deep learning architectures
* 🌦️ Real-time weather visibility enhancement
* 🎬 Faster video processing
* 🎨 Enhanced UI/UX experience

---

## ▶️ Running the Project

### Terminal 1 — Backend

```powershell
cd C:\Users\hp\Downloads\image-dehazing-main\backend

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

.\.venv\Scripts\Activate.ps1

python app.py
```

Expected Output:

```text
Running on http://127.0.0.1:8000
```

### Terminal 2 — Frontend

```powershell
cd C:\Users\hp\Downloads\image-dehazing-main\frontend

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

npm run dev
```

Expected Output:

```text
Local: http://localhost:5173
```

### 🌐 Open in Browser

```text
http://localhost:5173
```

---

⭐ If you found this project interesting, feel free to explore, fork, and contribute to AlertVision!
