# 🤖 Smart Neck-Assist Robot for Cervical Rehabilitation

![ESP32](https://img.shields.io/badge/ESP32-Microcontroller-blue?style=flat-square&logo=espressif)
![DOF](https://img.shields.io/badge/DOF-3--Axis-green?style=flat-square)
![Control](https://img.shields.io/badge/Control-WiFi%20%7C%20Bluetooth-orange?style=flat-square)
![Weight](https://img.shields.io/badge/Weight-1.2kg-lightgrey?style=flat-square)
![Status](https://img.shields.io/badge/Status-Prototype%20Complete-brightgreen?style=flat-square)

> A cost-effective, wireless-controlled wearable robotic exoskeleton for neck rehabilitation targeting patients with Dropped Head Syndrome (DHS), ALS, and cervical spondylotic myelopathy.

---

## 🎥 Demo

<!-- Upload your demo video to the repo and replace the path below -->
## 🎥 Demo

### Wi-Fi Dashboard Control
https://github.com/user-attachments/assets/082f8974-8ca7-4abb-b3d2-ae807023513d

### Bluetooth Voice Control
https://github.com/YOUR_USERNAME/smart-neck-assist-robot/assets/YOUR_ASSET_ID/bluetooth_demo.mp4

---

## 📌 Overview

Traditional rigid cervical collars restrict natural neck motion, leading to muscle atrophy in **23% of long-term users**. They reduce flexion by **59%**, extension by **46%**, and lateral rotation by **18%**.

The **Smart Neck-Assist Robot** addresses this by providing:
- Dynamic 3-DOF neck movement instead of static immobilization
- Wireless control via Wi-Fi dashboard or Bluetooth voice commands
- Affordable, lightweight design at just **1.2 kg**
- Reduction in neck muscle fatigue by **40–60%** compared to unsupported conditions

---

## ⚙️ System Architecture

```
User Input (Wi-Fi Dashboard / Bluetooth Voice Command)
            ↓
    ESP32 Microcontroller
            ↓
    PWM Signal Generation
            ↓
  3x MG995 Servo Motors
            ↓
  3-DOF Mechanical Structure
  (Pitch · Roll · Yaw)
            ↓
  Neck Rehabilitation Assistance
```

---

## 🦾 Degrees of Freedom

| Motion | Axis | Range | Servo |
|--------|------|-------|-------|
| Flexion / Extension | Pitch | ±15° | Servo 1 + Servo 2 |
| Lateral Bending | Roll | ±30° | Servo 1 + Servo 2 |
| Axial Rotation | Yaw | ±75° | Servo 3 |

---

## 🔧 Hardware Components

| Component | Details |
|-----------|---------|
| Microcontroller | ESP32-WROOM-32 (Dual-core, 240MHz) |
| Servo Motors | MG995 — 10 kg·cm torque @ 4.8V (×3) |
| Power Supply | DC-DC Buck Converter (12V → 5V) |
| Display | I2C LCD (SDA: GPIO 21, SCL: GPIO 22) |
| Frame | Steel — lightweight & stable |

### ESP32 Pin Mapping

| Component | ESP32 Pin | Function |
|-----------|-----------|----------|
| Servo 1 | GPIO 15 | Pitch & Roll |
| Servo 2 | GPIO 4 | Pitch & Roll |
| Servo 3 | GPIO 5 | Yaw (Axial Rotation) |
| LCD SDA | GPIO 21 | I2C Data |
| LCD SCL | GPIO 22 | I2C Clock |
| Power | VIN | Common 5V bus |
| Ground | GND | Common ground |

---

## 🖥️ Control Interfaces

### 1. Wi-Fi Dashboard
- Accessible from any device (smartphone, tablet, laptop)
- No app installation required
- Buttons for: Right/Left, Up/Down, Rotation, Total Off

### 2. Bluetooth Voice Commands
- Via SriTu Hobby app
- Commands: `"side"`, `"front"`, `"rotate"`, `"stop"`
- Robust performance across different voice types and noise conditions
- Emergency stop available on both interfaces

---

## 📊 Results

| Motion | Achieved |
|--------|----------|
| Pitch (Flexion/Extension) | ✅ ±15° |
| Roll (Lateral Bending) | ✅ ±30° |
| Yaw (Axial Rotation) | ✅ ±75° |

- ✅ Smooth servo transitions across all 3 DOF
- ✅ 40–60% reduction in neck muscle fatigue vs. unsupported conditions
- ✅ Dual-control mode (caregiver-assisted ↔ patient-controlled)
- ✅ Consistent voice command recognition across noise environments
- ✅ Total system weight: **1.2 kg**

---

## 🔬 Calibration

Calibrated using an **MPU6050 gyroscope and accelerometer** attached to the chin lever to map servo motor angles to actual head displacement. Each axis independently verified for clean motion with minimal cross-axis coupling.

---

## 🚀 Future Work

- Integration of **EMG sensors** for muscle activity monitoring
- **FES (Functional Electrical Stimulation)** for active muscle engagement
- **AI-assisted adaptive therapy** based on patient progress
- **Cloud-based tele-rehabilitation** support
- Custom forehead/chin pads for improved comfort



---

## 🏷️ Tags

`Robotics` `ESP32` `Rehabilitation Engineering` `Wearable Robotics` `Servo Control` `Assistive Exoskeleton` `Embedded Systems` `Bluetooth` `WiFi` `3-DOF` `Cervical Rehabilitation`
