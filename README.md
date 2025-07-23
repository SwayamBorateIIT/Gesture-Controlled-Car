# 🤖 Gesture-Controlled Car

A wireless, gesture-controlled robotic car that responds to real-time hand tilt using an MPU6050 sensor. Built using Arduino and nRF24L01+ wireless modules, this project showcases embedded systems integration, motion sensing, and wireless communication.

## 📌 Overview

This project enables controlling a 4WD robotic car with hand gestures. The system uses:
- An **MPU6050 accelerometer and gyroscope** to detect hand tilt.
- An **Arduino Nano** to process motion data.
- An **nRF24L01+ module** for wireless communication.
- An **L298N motor driver** to drive the motors.

The car translates hand gestures into motor commands for direction and speed control in real time.

## 🔧 Hardware Components

### Transmitter (Glove Module)
- Arduino Nano  
- MPU6050 (Accelerometer + Gyroscope)  
- nRF24L01+ Transceiver  
- nRF Adapter  
- Breadboard & jumper wires  
- 7–12V Battery

### Receiver (Car Module)
- Arduino Nano  
- nRF24L01+ Transceiver  
- nRF Adapter  
- L298N Motor Driver  
- 4WD Car Chassis (with 4 DC gear motors)  
- Breadboard & jumper wires  
- 7–12V Battery

## 🧠 Working Principle

1. **Sensing Movement**: The MPU6050 detects hand tilt (pitch/roll) and sends angle data to the Arduino.
2. **Mapping Values**: Angle values are mapped to a range of 0–254 using the Arduino's `map()` function.
3. **Wireless Transmission**: Mapped values are sent to the car wirelessly using nRF24L01+ modules (via SPI).
4. **Receiving & Processing**: The receiver Arduino reads the data, maps it to -255 to 255, and calculates motor speeds.
5. **Motor Control**: The L298N driver adjusts direction and speed of the motors based on the gesture.

## 🚗 Features

- Real-time gesture-based control
- Smooth directional steering and speed variation
- Reliable wireless communication
- Modular transmitter and receiver architecture

## 📂 File Structure

```plaintext
Gesture-Controlled-Car/
├── Transmitter/
│   └── transmitter_code.ino
├── Receiver/
│   └── receiver_code.ino
├── README.md
└── Documentation/
    └── ES116_Final_Project.pdf
