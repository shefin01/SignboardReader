---

# 🧠 Real-Time Smart Signboard Reader for the Visually Impaired

## 🎯 Purpose

A real-time system that detects traffic signboards, reads any visible text, and speaks it out loud — built to assist visually impaired individuals or anyone unable to read signboards while navigating.

---

## 🛠 Tech Stack

- *YOLOv8 (Ultralytics):* For signboard detection  
- *EasyOCR:* For reading text on the signboards  
- *gTTS + PyDub + pygame:* For converting text to speech  
- *OpenCV:* For video capture and display  
- *Python (Jupyter Notebooks):* Development environment  

---

## 📂 Repository Contents

| File | Description |
|------|-------------|
| best.pt | Custom-trained YOLOv8 model for traffic signboard detection |
| run_app.ipynb | Main notebook to run detection, OCR, and TTS |
| yolo_training.ipynb | Full notebook to train YOLOv8 on Roboflow dataset |
| requirements.txt | All Python dependencies needed to run the project |

---

## 📸 How It Works (Simple Flow)

1. *Camera Feed:* Captures video using phone or laptop camera  
2. *YOLOv8 Detection:* Detects signboards in real-time  
3. *EasyOCR:* Reads visible text inside detected signs  
4. *TTS (gTTS + PyDub):* Speaks the text (or class label if no text)  
5. *Output:* Live video with bounding boxes + audio feedback  

---

## 🧠 Deep Learning Components

- *YOLOv8:* Custom-trained deep neural network that detects signboards using learned features (shape, color, pattern)
- *EasyOCR:* Uses deep learning (CRNN + CTC) to read text from signboards, even when distorted or tilted

---

## ✅ YOLOv8 Training Details

- *Dataset Source:* [Signboard Detector on Roboflow](https://universe.roboflow.com/fin-maxwc/signboard-detector-bcyrz)
- *Images:* ~43,000 labeled images in YOLO format
- *Training Platform:* Google Colab with T4 GPU
- *Epochs:* 10
- *Exported Model:* best.pt (best-performing checkpoint)

> Note: The Roboflow dataset isn't included here due to size. You can access and export it yourself from the link above.

---

## 🚀 Future Plans

- 📱 Mobile or web app version with accessible UI  
- ⚡ Faster inference using YOLOv8n / ONNX / TFLite  
- 🌍 Support for multilingual OCR and TTS  
- 🧠 Smarter detection fallback if OCR fails  
- ☁ Streamlit / Hugging Face demo hosting  
- 📊 Expand dataset with region-specific signs  

---

## 🧰 Setup Instructions

1. *Clone the repo*

git clone https://github.com/your-username/SignboardReader.git
cd SignboardReader

3. Install dependencies



pip install -r requirements.txt

3. Install ffmpeg (for audio support via PyDub)



# Ubuntu/Debian
sudo apt install ffmpeg

# Mac (using Homebrew)
brew install ffmpeg

# Windows
Download from: https://ffmpeg.org/download.html


---

▶ Running the App

1. Open run_app.ipynb in Jupyter Notebook


2. Make sure your phone is connected as a webcam


3. Run all cells


4. The system will detect signboards, read any text, and speak it out



> Adjust cv2.VideoCapture(1) if needed (e.g., use 0 for laptop cam)





---

🔗 Credits

Ultralytics YOLOv8

EasyOCR

Roboflow Dataset



---

👨‍💻 Author

Mohammed Shefin
Reach out for collaboration, suggestions, or contributions.

---
