<h1 align="center">DecodeLabs internship — IoT Projects</h1>
<p align="center">A collection of embedded and IoT systems projects built on the ESP32, developed as part of the <b>DecodeLabs Internship</b> program.</p>

<p align="center">
  <img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white" />
  <img src="https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white" />
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" />
</p>

---

## 📖 About

This repository documents my embedded systems work from the Decode Internship program. Each project is a self-contained ESP32 sketch covering sensors, displays, and real-time control logic — built to demonstrate practical IoT and automation skills.

---

## 🚀 Projects

### 1. [Home Automation System](./home-automation)
Real-time temperature & humidity monitor with multi-output alerting across LCD, OLED, RGB LED, and a NeoPixel ring.

### Features

- Live temp/humidity readings every 2s
- 3-level alerts: Safe → Warning → Danger
- RGB LED + NeoPixel animations (solid/pulse/spin)
- LCD + OLED dual display with bar graphs
- Sensor failure detection with alert flash

### Tech Stack
ESP32 (C++/Arduino)   - DHT sensor library    - Adafruit NeoPixel   - LiquidCrystal_I2C   - Adafruit GFX/SSD1306

### Hardware

ESP32   - DHT22   - 16x2 I2C LCD   - SSD1306 OLED   - RGB LED   - NeoPixel Ring (16)   - Buzzer

### Usage

Power on the board — the boot animation runs, then the system continuously reads sensor data and updates all displays/LEDs every 2 seconds based on the current temperature/humidity alert level.

### Simulation Link
https://wokwi.com/projects/467456743862522881

![Project Image](IMAGES/SMART%20HOME.jpeg)

---

### 2. [Smart Irrigation System](./smart-irrigation)
Automated soil-moisture-based irrigation system with auto/manual pump control, crop temperature recommendations, and tank-level monitoring.

### Features

- Soil moisture sensing with auto pump ON/OFF
- Manual/Auto mode toggle via push button
- Tank-level monitoring with critical-low shutoff + alert
- Crop temperature recommendation
- Fertility level estimate from soil moisture
- 3-color RGB soil status
- Rotating 4-screen LCD display + full OLED dashboard
-  Distinct buzzer alert patterns for tank-critical vs soil-dry

### Tech Stack

ESP32 (C++/Arduino)   - DHT sensor library   - Adafruit GFX/SSD1306   - LiquidCrystal_I2C

### Hardware

ESP32 - DHT22 - Soil Moisture Sensor - Relay Module - 16x2 I2C LCD - SSD1306 OLED - RGB LED - Buzzer - Push Button

### Usage

- On boot, OLED and LCD show startup screens.
- System starts in AUTO mode — pump activates automatically based on soil dryness.
- Press the mode button to toggle AUTO/MANUAL.
- LCD rotates through 4 screens: Soil & Tank, Pump & Alert, Climate, Agri Info.
- Buzzer sounds three short beeps for tank-critical, one long beep for dry soil.
- Open Serial Monitor at 115200 baud for detailed logs.

### Simulation Link
https://wokwi.com/projects/467360922124136449

![Project Image](IMAGES/Smart%20Irrigation%20System.jpeg)

---
