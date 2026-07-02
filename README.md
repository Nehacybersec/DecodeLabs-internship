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
### 3. [Cloud-Connected security home system](./Cloud-Connected security home system)
A cloud-connected physical security telemetry system built on ESP32.Detects intruders, fire, gas leaks, and motion — with instant phone alerts.

### Features

- Detects intruders using an HC-SR04 ultrasonic sensor and PIR motion sensor, triggering instant alerts when someone enters within 80 cm.
- Monitors gas and smoke levels via the MQ-2 sensor and automatically activates a relay to cut the gas supply on dangerous readings.
- Detects open flames using an infrared flame sensor and raises a pre-fire warning via DHT22 temperature spike detection above 50 °C.
- Displays live sensor readings and threat level on a local SSD1306 OLED display — works even without internet.
- Plays distinct buzzer melodies for each threat level — a chime for all clear, beeps for caution, and a rapid siren for critical alerts.
- Controls two relay modules to trigger a gas valve, indoor alarm, or outdoor siren automatically based on threat severity.
- Streams all telemetry to Blynk IoT for real-time mobile push notifications and to Adafruit IO for cloud data logging and email alerts.
- Arm and disarm the system using a physical push button or remotely from the Blynk mobile app from anywhere in the world.

### Tech Stack

ESP32 Arduino Core v3 · Blynk IoT · Adafruit IO · MQTT / PubSubClient · I²C / ADC / DAC / PWM · Wokwi Simulator

### Hardware

ESP32 ,  HC-SR04,   PIR sensor,    MQ-2 gas sensor,    flame sensor,   DHT22,   SSD1306 OLED,  buzzer,  2× relay module

### Usage

- Home security — detects intruders at doors, windows, and hallways and alerts you instantly on your phone
- Fire safety — catches a flame or dangerous heat rise before it spreads and sounds a local siren
-  Gas leak protection — detects LPG or smoke and automatically shuts a solenoid gas valve via relay
- IoT learning — demonstrates Wi-Fi telemetry, MQTT protocol, cloud dashboards, and sensor fusion on ESP32
- Smart automation — remote arm/disarm, relay control, and live monitoring from anywhere via Blynk app
### Simulation Link
https://wokwi.com/projects/468040117704727553

![Project Image]()

---
