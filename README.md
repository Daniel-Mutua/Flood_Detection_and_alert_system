[FloodGuard_README.md](https://github.com/user-attachments/files/25135864/FloodGuard_README.md)
# FloodGuard – Smart Flood Detection, Alert & Evacuation System

## Overview
FloodGuard is an intelligent flood detection and evacuation system built using the ESP8266 platform.  
It combines real-time water level monitoring, visual web-based dashboards, alert mechanisms, and an automated evacuation motor to enhance safety during flood events.

## Key Features
- Real-time water level sensing using an analog sensor  
- ESP8266 Access Point with live web dashboard  
- Visual live graph, flood history, and prediction pattern  
- Automatic flood alerts with LED and buzzer  
- Manual emergency buzzer control from the dashboard  
- Automated evacuation motor with safe state-machine control  
- Manual evacuation trigger via web interface  
- Non-blocking timing for reliable system performance  

## Motor Evacuation Logic
For each flood event, the evacuation motor follows a safe and deterministic sequence:
1. Forward movement for 3 seconds  
2. Pause for 3 seconds  
3. Backward movement for 3 seconds  
4. Pause for 3 seconds  

This completes one evacuation cycle.  
The system performs exactly **three cycles per flood event**, then stops automatically.

## Hardware Components
- ESP8266 (ESP-12E / NodeMCU)  
- Analog water level / rain sensor  
- DC motor with motor driver (ENA, IN1, IN2)  
- Green LED (safe indicator)  
- Red LED + buzzer (alert indicator)  
- External power supply for motor  

## Pin Configuration
- Water Sensor: A0  
- Green LED: D6  
- Alert LED + Buzzer: D7  
- Motor ENA: D5  
- Motor IN1: D1  
- Motor IN2: D2  

## Network Access
- WiFi SSID: FloodGuard-ESP  
- Password: 12345678  
- Access the dashboard using the IP address shown on the Serial Monitor after boot.

## Use Cases
- Flood-prone residential areas  
- River basin monitoring demonstrations  
- Smart disaster management projects  
- Engineering competitions and exhibitions  

## Safety & Design Notes
- The system uses non-blocking timing to ensure sensor readings and alerts are never interrupted.  
- Manual controls are provided to override automation in emergency situations.  
- The architecture is scalable for future integration with cloud platforms, GPS, or AI-based prediction models.

## Author
FloodGuard – Smart Disaster Response System  
Developed for academic and competition demonstration purposes.
