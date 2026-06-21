# DecodeLabs-internship
End-to-end, project-based IoT repository showcasing work completed during the Decode Lab Internship.

#1. ESP32 Home Automation System

Real-time temperature & humidity monitor using DHT22, displayed across LCD, OLED, RGB LED, and a NeoPixel ring.

Features


Live temp/humidity readings every 2s
3-level alerts: Safe → Warning → Danger
RGB LED + NeoPixel animations (solid/pulse/spin)
LCD + OLED dual display with bar graphs
Sensor failure detection with alert flash


Tech Stack

ESP32 (C++/Arduino) · DHT sensor library · Adafruit NeoPixel · LiquidCrystal_I2C · Adafruit GFX/SSD1306

Hardware

ESP32 · DHT22 · 16x2 I2C LCD · SSD1306 OLED · RGB LED · NeoPixel Ring (16) · Buzzer


