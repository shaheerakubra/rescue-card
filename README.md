# rescue-card
Rescue Card — IoT Safety Device for Vulnerable Populations
A wearable personal safety system embedded in an ID card form factor, designed to protect vulnerable individuals (elderly, children, people with disabilities) without drawing attention or suspicion.

📌 Overview
Rescue Card is an academic group project built to address a real-world safety gap: vulnerable individuals often cannot discreetly call for help in dangerous situations. By embedding safety features inside a standard ID card, the device blends into everyday life while providing powerful emergency response capabilities.

✨ Features
Feature Description 
GPS Geolocation, 
Real-time location tracking transmitted to emergency contacts 
Fall Detection: Accelerometer-based automatic detection of sudden falls
SOS Button: One-touch emergency calling to pre-configured contacts 
Loud Buzzer Alert, High-decibel sound alarm to deter threats and attract attention
ID Card Form Factor: Disguised as a standard ID card — avoids theft or suspicion

🛠️ Tech Stack

Hardware: Arduino microcontroller, GPS module, accelerometer, GSM module, piezo buzzer
Backend: Python
Communication: Hardware-to-software serial communication between Arduino and Python backend
Other: SMS/call triggering via GSM for emergency alerts


System Architecture
[Arduino Hardware Layer]
        |
   Sensors (GPS, Accelerometer, Button, Buzzer)
        |
   Serial Communication
        |
[Python Backend Layer]
        |
   Emergency Logic (fall detection threshold, SOS trigger)
        |
   GSM Module → Emergency Call / SMS to contacts

👥 Team
Built as an academic group project (3+ members) as part of the Bachelor of Technology in Information Technology program at Muffakham Jah College of Engineering and Technology.
Shaheera Kubra — Python backend development, system integration

Motivation
Vulnerable populations — including the elderly, children, and individuals with disabilities — often face situations where they cannot openly ask for help. Existing solutions like panic buttons or smartwatches are conspicuous and easily identified (and removed) by bad actors. Rescue Card solves this by hiding full emergency functionality inside something nobody would ever question: an ID card.

Getting Started
Prerequisites

Arduino IDE
Python 3.x
Required Python libraries:

bashpip install pyserial
Hardware Required

Arduino Uno or Nano
NEO-6M GPS Module
ADXL345 Accelerometer
SIM800L GSM Module
Piezo Buzzer
Push button

Setup

Clone this repository

bashgit clone https://github.com/yourusername/rescue-card.git

Upload the Arduino sketch (rescue_card.ino) to your Arduino board via Arduino IDE
Update config.py with your emergency contact numbers
Run the Python backend:

bashpython main.py

Project Structure
rescue-card/
├── arduino/
│   └── rescue_card.ino       # Arduino sketch (hardware control)
├── backend/
│   ├── main.py               # Main Python backend
│   ├── fall_detection.py     # Fall detection logic
│   ├── gps_tracker.py        # GPS parsing and location logic
│   └── emergency_call.py     # GSM call/SMS trigger
├── config.py                 # Emergency contacts configuration
└── README.md

License
This project was developed for academic purposes. Feel free to build on it for research or non-commercial use.

Contact
Shaheera Kubra

Email: shaheerakubra03@gmail.com
LinkedIn: linkedin.com/in/shaheera-kubra-6aa917229
