# 💧 IoT-based Village Water Control System

This project is a smart water control and monitoring system designed for rural and village water supply management. It uses an **ESP32** microcontroller, **Firebase Realtime Database**, and a **mobile application built using MIT App Inventor** to remotely control water flow and monitor status.

---

## 📱 Features

- Remotely control village water motor/pump via mobile app
- Real-time monitoring of water motor status (ON/OFF)
- Firebase integration for cloud control and data storage
- Easy-to-use Android app (developed with MIT App Inventor)
- Low cost and scalable solution for rural water management

---

## 🧠 System Architecture

[Mobile App]
|
[Firebase Realtime Database]
|
[ESP32]
|
[Relay Module] ----> [Water Pump]

yaml
Copy
Edit

---

## 🔧 Hardware Components

- ESP32 Development Board
- Relay Module (5V)
- Water Pump or Solenoid Valve
- Power Supply
- Optional: Flow sensor, LCD display, etc.

---

## 🧪 Software & Tools

- Arduino IDE (with ESP32 board support)
- Firebase Realtime Database
- MIT App Inventor
- Firebase Arduino Library

---

## 🚀 How It Works

1. The mobile app sends commands (ON/OFF) to Firebase.
2. ESP32 continuously listens to Firebase for changes.
3. When the database value changes, ESP32 activates/deactivates the relay connected to the water pump.
4. ESP32 also updates the real-time status back to Firebase for monitoring on the app.

---

## 📂 Project Structure

IoT-based-Village-Water-Control-system/
├── ESP32_Code/
│ └── water_control.ino
├── Mobile_App/
│ └── aia_file_for_MIT_App_Inventor.aia
├── firebase_setup.md
├── circuit_diagram.png
└── README.md

yaml
Copy
Edit

---

## 🔌 Firebase Setup

1. Create a Firebase project at [firebase.google.com](https://firebase.google.com/)
2. Enable Realtime Database and set rules to:
   ```json
   {
     "rules": {
       ".read": "true",
       ".write": "true"
     }
   }

cpp
Copy
Edit
Firebase.begin(FIREBASE_HOST, FIREBASE_AUTH);
📲 Mobile App (MIT App Inventor)
Drag and drop buttons for ON/OFF

Use Firebase component to update value

Display motor status dynamically
![image](https://github.com/user-attachments/assets/c052e12e-c118-410c-b54a-3c73e8160837)


