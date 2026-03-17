# Robotic-dog
# Robotics Project: Robotic Dog

## Introduction
A robotic dog is a biomimetic robot designed to imitate the movement and behavior of a real dog. It can walk, respond to commands, and perform actions using sensors and programmed logic.

---

## Objective
To design and build a robotic dog that can walk, detect obstacles, and respond to basic commands using sensors and actuators.

---

## Components Required
- Arduino Uno / Raspberry Pi  
- Servo Motors (8–12 for legs)  
- Ultrasonic Sensor  
- Bluetooth Module (HC-05)  
- Motor Driver / Servo Controller  
- Battery Pack  
- Chassis (3D printed or DIY frame)  
- Jumper Wires  

---

## Working Principle
The robotic dog uses servo motors to control leg movement. A programmed sequence controls walking patterns. Sensors help detect obstacles, and a Bluetooth module allows control via a smartphone.

---

## Features
- Walking and turning movements  
- Obstacle detection  
- Remote control via mobile  
- Can simulate dog-like actions (sit, stand)  

---

## Circuit Connections
- Servo Motors → Connected to PWM pins  
- Ultrasonic Sensor:
  - VCC → 5V  
  - GND → GND  
  - Trig → Pin 9  
  - Echo → Pin 10  
- Bluetooth Module:
  - TX → RX  
  - RX → TX  

---

## Algorithm
1. Initialize all servo motors  
2. Execute walking sequence (predefined angles)  
3. Continuously check for obstacles  
4. If obstacle detected → stop or turn  
5. Receive commands via Bluetooth  
6. Perform actions based on input  

---

## Sample Code (Basic Servo Movement)
```cpp
#include <Servo.h>

Servo leg1;

void setup() {
  leg1.attach(9);
}

void loop() {
  leg1.write(0);   // Move to 0°
  delay(1000);
  leg1.write(90);  // Move to 90°
  delay(1000);
}
