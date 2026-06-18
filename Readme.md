Terminal 1 — Backend
cd C:\Users\hp\Downloads\image-dehazing-main\backend
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
python app.py

You should see:

Running on http://127.0.0.1:8000
Terminal 2 — Frontend
cd C:\Users\hp\Downloads\image-dehazing-main\frontend
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
npm run dev

You should see:

Local: http://localhost:5173

Then open:

http://localhost:5173



Project Overview

“This project removes haze/fog from images and videos using deep learning and image processing techniques. It has a React frontend and a Python Flask backend. The backend loads a trained PyTorch model and processes uploaded media to improve visibility and image clarity.”

Technologies Used
Frontend

Your frontend uses:

Technology	Purpose
React	UI development
TypeScript	Type-safe frontend code
Vite	Fast frontend build tool
Tailwind CSS	Styling
Axios	API calls to backend
React Dropzone	File upload UI

Your package.json clearly shows React, Vite, TypeScript, Axios, Tailwind, Zustand, etc.

Your frontend starts from:

src/main.tsx

because index.html loads it.

Your project also uses:

vite.config.ts
tailwind.config.ts
postcss.config.js

for Vite + Tailwind setup.

Backend

Your backend uses:

Technology	Purpose
Python	Main backend language
Flask	Backend web server/API
Flask-CORS	Frontend-backend communication
PyTorch	Deep learning inference
OpenCV	Image/video processing
NumPy	Matrix operations
Pillow (PIL)	Image handling
Matplotlib	Visualization utilities

Backend files:

app.py
model.py
utils.py
AI / Deep Learning Part

Your project uses:

Component	Purpose
PyTorch	Loading trained model
Pretrained .pk model	Learned haze removal
CNN-based dehazing model	Image restoration
Feature Fusion Attention	Deep learning dehazing method

The model file:

net/trained_models/its_train.pk

is the trained checkpoint.

You also provide another classical method:

Dark Channel Prior

which is a traditional computer vision algorithm.

So your project supports:

Traditional image processing
Deep learning based dehazing

That is actually a strong point.

Architecture

You can explain architecture like this:

Frontend (React + Vite)
        ↓
Axios API request
        ↓
Flask Backend
        ↓
PyTorch Model + OpenCV Processing
        ↓
Processed Image Returned
        ↓
Frontend Displays Output
How the Project Works

Say this:

“The user uploads a hazy image or video through the React frontend. The frontend sends the file to the Flask backend using an HTTP POST request. The backend loads the image, preprocesses it, passes it through a dehazing model built using PyTorch, generates the enhanced output, and returns the processed file back to the frontend.”

Two Models Used
1. Dark Channel Prior (Traditional CV)

Say:

“Dark Channel Prior is a classical image processing method for haze removal based on atmospheric scattering assumptions.”

Good point:

No training required
Rule-based image restoration
Traditional computer vision approach
2. Feature Fusion Attention (Deep Learning)

Say:

“Feature Fusion Attention is a CNN-based deep learning model that learns haze removal patterns from training data.”

Good keywords:

CNN
Feature extraction
Attention mechanism
Image restoration
Deep learning inference
Why Flask?

Say:

“Flask is lightweight and easy for building REST APIs. It connects the frontend and AI model efficiently.”

Why React + Vite?

Say:

“React provides reusable UI components and Vite gives very fast frontend development and hot reloading.”

Why PyTorch?

Say:

“PyTorch is widely used for deep learning research and model inference. It makes loading pretrained models easy.”

Why OpenCV?

Say:

“OpenCV is used for image and video preprocessing, frame handling, resizing, and manipulation.”

File Flow
Frontend
User uploads image
↓
Uploader component
↓
Axios POST request
↓
localhost:8000/dehaze
Backend
Flask receives file
↓
OpenCV/PIL loads image
↓
PyTorch model processes image
↓
Result generated
↓
Flask sends processed image back
Concepts Used

You can say your project uses:

Full-stack development
REST API
Frontend-backend integration
Deep learning inference
Computer vision
Image processing
File handling
HTTP POST requests
Model loading
Image enhancement
Important Interview Terms

Use these confidently:

Image Restoration
Dehazing
Computer Vision
CNN
Deep Learning
Inference
Feature Extraction
Attention Mechanism
REST API
Flask API
Frontend-Backend Communication
OpenCV Processing
PyTorch Model Loading
Important Files
Frontend
File	Purpose
src/main.tsx	React entry point
Uploader.tsx	Upload component
package.json	Dependencies
vite.config.ts	Vite configuration
tailwind.config.ts	Styling config
Backend
File	Purpose
app.py	Flask server
model.py	AI model loading/inference
utils.py	Helper functions
trained_models/*.pk	Trained weights
Problems You Solved

This is very important in interview.

You can say:

“I handled Python environment setup, frontend-backend integration, PyTorch compatibility issues, dependency conflicts, model loading problems, and REST API communication.”

That actually sounds impressive because you genuinely debugged them.

Limitations

Be honest:

Model quality depends on training
Heavy processing for large videos
CPU inference is slower
Some haze types may not clear perfectly
Future Improvements

Say:

Use better datasets
Train larger models
Add GPU acceleration
Deploy on cloud
Improve UI
Add real-time webcam dehazing
Optimize video processing speed