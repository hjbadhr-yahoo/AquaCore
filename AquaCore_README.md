# 💧 AquaCore — Smart Water Tank Monitoring System

<div align="center">

![AquaCore Banner](https://img.shields.io/badge/AquaCore-Smart%20Water%20Monitor-00aaff?style=for-the-badge&logo=arduino)
![Author](https://img.shields.io/badge/Author-Harsh%20Jangra-ff6600?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-ESP32%20%7C%20ESP32--S3-green?style=for-the-badge&logo=espressif)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

### Designed & Developed by **Harsh Jangra**
#### Electronics & IoT Engineer | Punjab, India

</div>

---

## 👨‍💻 Author

| | |
|---|---|
| **Name** | **Harsh Jangra** |
| **GitHub** | [@hjbadhr-yahoo](https://github.com/hjbadhr-yahoo) |
| **Location** | Gharuan, Punjab, India |
| **Specialization** | Embedded Systems, IoT, ESP32, LoRa, Web Dashboards |

> ⚠️ This project was fully designed and developed by **Harsh Jangra**. Please credit the author if you use or modify this project.

---

## 📖 Project Overview

**AquaCore** is a two-unit LoRa-based smart water tank monitoring system built on ESP32/ESP32-S3. It provides real-time water level monitoring, automated pump control, and a beautiful animated web dashboard — all accessible globally via ngrok.

### ✨ Key Features

- 📡 **LoRa Wireless Communication** between two ESP32 units
- 💧 **Real-time Water Level Monitoring** with ultrasonic sensor
- 🔄 **Automated Relay Pump Control** with manual override
- 📟 **OLED Display** showing live status on the device
- 🌐 **Animated Web Dashboard** accessible from any device
- 🌍 **Global Access** via ngrok tunnel
- 🔔 **Alert System** for low/high water levels

---

## 🛠️ Hardware Components

| Component | Specification | Quantity |
|-----------|--------------|----------|
| Microcontroller | ESP32 (Sender Unit) | 1 |
| Microcontroller | ESP32-S3 (Receiver Unit) | 1 |
| LoRa Module | SX1276 / Ra-02 (433MHz) | 2 |
| Ultrasonic Sensor | HC-SR04 | 1 |
| OLED Display | 0.96" SSD1306 (128x64) | 1 |
| Relay Module | 5V Single Channel | 1 |
| Water Pump | 12V DC Submersible | 1 |
| Power Supply | 5V/3.3V | 2 |

---

## 📁 Project Structure

```
AquaCore/
├── src/
│   ├── sender/
│   │   └── sender.ino          # ESP32 Sender firmware
│   └── receiver/
│       └── receiver.ino        # ESP32-S3 Receiver firmware
├── diagrams/
│   ├── circuit_diagram.png     # Full circuit schematic
│   └── system_architecture.png # System block diagram
├── docs/
│   └── project_report.pdf      # Full project documentation
├── README.md
└── LICENSE
```

---

## ⚙️ How It Works

```
[Water Tank]
     |
[HC-SR04 Ultrasonic Sensor]
     |
[ESP32 Sender Unit]  ──LoRa──►  [ESP32-S3 Receiver Unit]
                                        |
                              ┌─────────┴──────────┐
                              │                    │
                         [OLED Display]     [Web Dashboard]
                                                   |
                                           [Relay Pump Control]
```

1. **Sender Unit** reads water level via ultrasonic sensor every 2 seconds
2. Data is transmitted wirelessly via **LoRa (433MHz)**
3. **Receiver Unit** gets data, shows it on OLED display
4. **Web Dashboard** displays animated real-time level with pump control
5. Pump auto-triggers based on configured thresholds

---

## 🌐 Web Dashboard Features

- Animated water tank visualization
- Real-time level percentage display
- Manual pump ON/OFF control
- Auto/Manual mode switching
- Alert notifications
- Mobile responsive design

---

## 📦 Libraries Required

```
- LoRa by Sandeep Mistry
- Adafruit SSD1306
- Adafruit GFX Library
- ESPAsyncWebServer
- AsyncTCP
- ArduinoJson
```

---

## 🚀 Setup & Installation

1. Clone this repository
```bash
git clone https://github.com/hjbadhr-yahoo/AquaCore.git
```

2. Open sender firmware in Arduino IDE
3. Install all required libraries
4. Configure your WiFi credentials in `receiver.ino`
5. Upload sender code to ESP32
6. Upload receiver code to ESP32-S3
7. Power both units and access the web dashboard

---

## 📸 Circuit Diagram

> See `/diagrams/circuit_diagram.png` for full schematic

---

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

**Created by Harsh Jangra** — Feel free to use, modify, and share with proper credit.

---

<div align="center">

**⭐ If this project helped you, please give it a star! ⭐**

Made with ❤️ by **Harsh Jangra** | Punjab, India

</div>
