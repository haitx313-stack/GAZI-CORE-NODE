# GAZI CORE ROOM NODE

## Overview
The GAZI Core Room Node is an embedded multi-sensor automation system designed to monitor environmental conditions, detect hazards, and perform automated responses in a room-level smart node architecture.

It is built using Arduino uno and integrates multiple sensors for real-time monitoring and decision-based control.

This system is part of the larger GAZI CORE ecosystem.

---

## Core Objectives
- Real-time environmental monitoring
- Gas leakage detection system
- Proximity-based automation
- Visual and audio alert system
- LCD-based live data interface
- Modular upgrade-ready architecture

---

## System Components

### Controller
- ARDUINO UNO (Main processing unit)

### Sensors
- DHT11 (Temperature & Humidity)
- MQ Gas Sensor (Air quality / gas detection)
- HC-SR04 Ultrasonic Sensor (Distance detection)
- IR Sensor (Reset / trigger input)

### Output Devices
- LCD 16x2 (I2C interface)
- RGB LED Module (Status indicator)
- Buzzer (Alert system)
- HC-05/6
- Built-in ESP32 LED (Simulation light control)

---

## Working Principle

 1. Boot Sequence
- System initializes sensors
- LCD displays startup message
- Buzzer gives startup beep

---

2. Monitoring Mode
- Continuously reads:
  - Temperature
  - Humidity
  - Gas levels
  - Distance

---

3. Gas Alert Mode
If gas threshold is exceeded:
- RGB LED turns RED
- Buzzer activates alert pattern
- LCD displays warning message
- System waits for IR reset signal

---

 4. Light Control Logic
- If object detected (ultrasonic < threshold):
  → Light turns ON

- If IR sensor triggered:
  → Light turns OFF

---

 5. Normal Mode
- RGB LED stays GREEN
- LCD shows live sensor data
- System continues monitoring loop

---

 System Architecture
ARDUINO acts as central controller managing:
- Sensor input processing
- Decision logic execution
- Output device control
- Real-time system updates

---

Limitations
- No advanced filtering for sensor noise
- Delay-based timing (not real-time optimized)
- No wireless control interface yet
- Basic LCD UI only

---

Future Improvements

 Phase 2
- Bluetooth control system (mobile integration)
- Manual override system
- Real-time data logging

Phase 3
- State machine architecture (no delay-based loops)
- Sensor calibration system
- Noise filtering algorithms

 Phase 4
- AI-based environmental prediction
- Smart automation rules engine
- Multi-node networking (GAZI CORE mesh system)

## Status
Prototype Stage – Functional Embedded Node System
