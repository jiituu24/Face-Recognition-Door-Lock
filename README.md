# Camera Face Recognition Door Lock

An ESP32-CAM based Smart Door Lock System that uses face detection and face recognition to unlock a door automatically for authorized users.

This project combines computer vision, IoT, and embedded systems to create a secure and contactless access control system. It uses the ESP32-CAM module to capture faces, process recognition locally, and trigger a locking mechanism when a known face is detected.

---

## 🚀 Features

- 📷 Real-time camera streaming through browser
- 😀 Face detection
- 🧠 Face recognition
- 🔓 Automatic door unlock for authorized users
- 🚨 Intruder alert for unknown faces
- 🌐 Web interface for camera feed and controls
- ⚡ Runs on ESP32-CAM hardware
- 💾 Stores multiple face IDs

---

## 🛠 Hardware Required

- ESP32-CAM Module (AI Thinker recommended)
- FTDI Programmer / USB to TTL Converter
- Servo Motor / Solenoid Lock / Relay Module
- Jumper Wires
- 5V Power Supply
- Door Lock Mechanism

---

## 📂 Project Files

### CameraFaceRecognitionDoorLock.ino
Main Arduino sketch containing:
- WiFi connection
- Camera initialization
- Door lock control logic
- Face recognition trigger actions

### app_httpd.cpp
Handles:
- Web server
- Camera streaming
- Face detection
- Face recognition
- Face enrollment
- HTTP routes

### camera_pins.h
Contains GPIO pin mapping for supported ESP32-CAM boards.

### camera_index.h
Contains embedded HTML page for web interface.

---

## ⚙️ How It Works

1. ESP32-CAM starts and connects to WiFi.
2. User opens ESP32 IP address in browser.
3. Camera stream becomes available.
4. User enrolls authorized faces.
5. When a face is detected:
   - If recognized → unlock door
   - If unknown → deny access

---

## 🔌 Wiring

Use ESP32-CAM normally.

For lock control, use any available GPIO pin connected to:

- Relay Module
- Servo Motor
- Solenoid Lock

---

## 📶 Setup Instructions

### 1️⃣ Install Arduino IDE

Install:
- ESP32 Board Package
- Required camera libraries

### 2️⃣ Select Board

Choose:

AI Thinker ESP32-CAM

### 3️⃣ Enter WiFi Credentials

```cpp
const char* ssid = "YourWiFi";
const char* password = "YourPassword";
