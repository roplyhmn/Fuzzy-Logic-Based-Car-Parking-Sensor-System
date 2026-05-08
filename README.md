# Fuzzy-Logic-Based-Car-Parking-Sensor-System

## Overview
This project implements a **smart car parking sensor system** using the **Mamdani Fuzzy Logic method** to provide more intuitive and gradual feedback to drivers during parking.  

Unlike conventional parking sensors that only provide binary outputs (ON/OFF), this system uses fuzzy logic to simulate human-like reasoning in evaluating object distance. The system adjusts LED colors and buzzer frequency dynamically based on obstacle proximity.

## Features
- Real-time distance measurement using ultrasonic sensor  
- Fuzzy Logic (Mamdani) implementation  
- Gradual parking feedback system  
- Dynamic RGB LED indicators  
- Adaptive buzzer frequency based on distance  
- More natural and intuitive driver assistance  

## Fuzzy Logic Concept

### Input Variable
- Distance from obstacle (0–200 cm)

### Output Variables
- RGB LED color
- Buzzer frequency

### Membership Functions
The system uses four fuzzy membership categories:
- Very Close
- Close
- Medium
- Far

## Fuzzy Rules

| No | IF (Distance) | THEN (Output) |
|---|---|---|
| 1 | Very Close | Red LED + Fast Buzzer |
| 2 | Close | Yellow LED + Medium Buzzer |
| 3 | Medium | Green LED + Slow Buzzer |
| 4 | Far | Green LED + Silent Buzzer |

## Inference Method
- Mamdani Fuzzy Inference System  
- MIN method for fuzzy AND operation  
- MAX method for output aggregation  
- Centroid (Center of Gravity) for defuzzification  

## Tech Stack
- Arduino Uno  
- Embedded C / Arduino C++  
- Fuzzy Logic (Mamdani)  
- Ultrasonic Sensor HC-SR04  
- RGB LED  
- Buzzer  
- Tinkercad Simulation  

## Hardware Components
- Arduino Uno R3  
- Ultrasonic Sensor HC-SR04  
- RGB LED  
- Passive Buzzer  
- Resistors  
- Breadboard & Jumper Wires  

## System Workflow
1. Ultrasonic sensor measures object distance  
2. Distance value enters fuzzification process  
3. Fuzzy inference rules determine output response  
4. Defuzzification calculates final LED and buzzer output  
5. System provides gradual visual and audio feedback

## Example Test Cases

### Case 1 — Distance = 20 cm
Output:
- LED → Orange/Red transition
- Buzzer → Fast frequency (~1850 Hz)

### Case 2 — Distance = 80 cm
Output:
- LED → Green
- Buzzer → Slow frequency (~1400 Hz)
