# objectdetectionusingMobileNetSSD_model
# 👁️ VisionAssist: AI Navigation & Object Detection for the Visually Impaired

> **Empowering independence through voice-controlled AI, real-time object recognition, and smart navigation.**

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/Computer_Vision-OpenCV-red?style=for-the-badge&logo=opencv&logoColor=white)
![Accessibility](https://img.shields.io/badge/Accessibility-Voice_Control-success?style=for-the-badge)

## 🌟 Executive Summary

**VisionAssist** is a sophisticated assistive technology tool designed to act as a digital "third eye" for blind or visually impaired individuals. 

By integrating **Computer Vision (MobileNetSSD)** with **Voice Command Logic**, this application interprets the visual world and converts it into auditory feedback. Whether it's identifying obstacles in a room, reading out the current location, or providing turn-by-turn navigation, VisionAssist helps users navigate their environment with confidence and safety.

## 🚀 Key Features

* **🗣️ Full Voice Control:** The entire system is hands-free. Users issue spoken commands to activate features, making it fully accessible.
* **📷 Real-Time Object Detection:** Uses the `MobileNetSSD` deep learning model to identify 20+ classes of objects (people, chairs, cars, etc.) and announces their position (left, right, center). 
* **📍 GPS Localization:** instantly announces the user's current street address using reverse geocoding.
* **🧭 Smart Navigation:** Integrates with the **OpenRouteService API** to calculate distances and provide foot-walking directions to specific destinations.
* **CONST🌤️ Live Weather Updates:** Fetches real-time temperature and weather descriptions from **OpenWeatherMap** for any city or the current location.

## 🎤 Voice Command Guide

The system listens for the following specific voice commands. Speak clearly into the microphone to trigger these actions:

| Command | Action Performed |
| :--- | :--- |
| **"Start detection"** | 🟢 **Activates** the camera and begins announcing objects detected in your path. |
| **"Stop detection"** | 🔴 **Deactivates** the object detection to save processing power or silence notifications. |
| **"Where am I?"** | 📍 Announces your current **GPS address** (Street, City, Zip). |
| **"Navigate to [Place]"** | 🧭 Calculates the distance and route to the destination (e.g., *"Navigate to Central Park"*). |
| **"Weather in [City]"** | 🌤️ Checks weather for a specific city (e.g., *"Weather in London"*). |
| **"Current weather"** | 🌡️ Checks the weather at your **current GPS location**. |
| **"Date and time"** | 📅 Announces the current day, date, and time. |
| **"Exit"** or **"Quit"** | ❌ Shuts down the application completely. |

## 🛠️ System Architecture

The application runs on a multi-threaded architecture to ensure smooth performance:
1.  **Main Thread:** Handles video capture and image processing.
2.  **Listener Thread:** Continuously listens for voice commands via the microphone.
3.  **Speaker Thread:** Queues text-to-speech outputs so audio doesn't freeze the video feed.

## ScreenShot:

<img width="1919" height="1079" alt="Screenshot 2025-09-06 081330" src="https://github.com/user-attachments/assets/3eeca124-22b5-4336-bb76-917349ffb0d3" />


## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/shankarin2k6/objectdetectionusingMobileNetSSD_model.git
cd objectdetectionusingMobileNetSSD_model
```

2. Install Dependencies
Install the required Python libraries using pip:
```bash
pip install opencv-python numpy pyttsx3 speechrecognition geopy openrouteservice requests pyaudio
```

3. Download Model Files (Crucial)
This project requires the Caffe MobileNetSSD model files. Download them and place them in the project root folder:

MobileNetSSD_deploy.prototxt.txt
MobileNetSSD_deploy.caffemodel

4. API Key Configuration
Open the main.py file and insert your own API keys to ensure the navigation and weather features work:
```
# In main.py
ORS_API_KEY = "YOUR_OPENROUTESERVICE_KEY"
OPENWEATHERMAP_API_KEY = "YOUR_OPENWEATHERMAP_KEY"
```

🏃‍♂️ How to Run
Simply execute the main python script:
```
python main.py
```
🔮 Future Roadmap
[ ] OCR Integration: Add a mode to read text from books or street signs.

[ ] Emergency SOS: Voice command to send GPS location to a family member.

[ ] Face Recognition: Identify saved friends or family members by name.

Thank You For Visiting!!

Developed By Shankari N













