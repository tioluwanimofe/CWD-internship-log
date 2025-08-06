# CWD-internship-log

# 🚋 Everzip Alpha Trolley – Sensor Integration & Remote Logging

This repository documents my work during the **Summer 2025 Engineering Internship** on the **Everzip Alpha Trolley** project. The focus was on integrating LiDAR and RFID sensors with the Arduino GIGA R1 WiFi, enabling real-time monitoring, logging, and control via a custom web dashboard. Additional work involved PCB design, LoRaWAN research, and team-based prototype development.

: 
                ----------------------------------------------------------------------------------------------------------------------------------
                | link to Electrical PCB designs: https://github.com/tioluwanimofe/CWD-everzip-alpha-trolley-electrical-design-by-Tio-Adesanya    |
                | link to Software Development Code: https://github.com/tioluwanimofe/trolley_testing_software-main_v-4-working-well              |
                ----------------------------------------------------------------------------------------------------------------------------------

## 📦 Features

- 🔧 **Sensor Integration**: LiDAR (TFMini) + RFID (RC522) + VESC motor control
- 🌐 **Local Web Dashboard**: Real-time UI served from the Arduino GIGA R1 for live monitoring
- ☁️ **Remote Data Logging**: Google Sheets + Serial + onboard JSON logs
- 📡 **LoRaWAN Research**: Early-stage integration with RAK3172 + ChirpStack
- 🧠 **Modular Codebase**: PlatformIO with environment-based test modes
- 🖥️ **Cross-Team Collaboration**: Firmware, hardware, welding, and dashboard design

---

## 🗂️ Project Structure

```bash
📁 everzip-firmware/
├── 📂 include/                  # Header files for modular subsystems
├── 📂 lib/                      # Libraries (RFID, LiDAR, Logging)
├── 📂 src/                      # Main code files
│   ├── main.cpp
│   └── WebServer.cpp
├── 📂 data/                     # HTML/CSS/JS for web UI (served via SPIFFS)
├── 📂 test/                     # Environment-specific test files
├── platformio.ini              # Build environments & board config
└── README.md                   # You are here
````

---

## 🚀 Getting Started

### ✅ Prerequisites

* [PlatformIO IDE](https://platformio.org/)
* Arduino GIGA R1 WiFi
* TFMini LiDAR, RC522 RFID module
* Google Sheets API credentials (optional)
* (For LoRaWAN) RAK3172, ChirpStack, Docker, WSL

### 🔌 Wiring Overview

| Component | Arduino Pin | Notes                |
| --------- | ----------- | -------------------- |
| TFMini    | Serial2     | Front & Rear support |
| RC522     | SPI         | RFID tag reader      |
| VESC RX   | PWM/Analog  | Motor speed control  |
| PCB IOs   | Custom      | As per schematic     |

### 🔧 Build & Upload

```bash
# Build project
pio run

# Upload firmware to GIGA R1 WiFi
pio run --target upload

# Monitor Serial Output
pio device monitor
```

---

## 🌐 Web Dashboard

* Serves real-time sensor data via `/dashboard` route
* Supports "Reset RFID" and "Reset Log" buttons
* Logs all data in JSON format to `/data.json`
* Easy integration with Google Sheets

<!-- [dashboard mockup](./assets/dashboard_preview.png) - Add your screenshot -->


## 📊 Data Logging

* **Serial Output**: Timestamped logs via USB
* **Google Sheets**: Optional HTTP POST via WiFi
* **Web View**: View logs at `/data.json` route

---

## 🛠️ Tools Used

| Tool/Tech         | Purpose                         |
| ----------------- | ------------------------------- |
| PlatformIO        | Embedded development            |
| KiCad             | PCB schematic & layout          |
| HTML/CSS/JS       | Web UI for sensor dashboard     |
| ESPAsyncWebServer | Arduino GIGA local server       |
| Google Sheets API | Remote test logging             |
| ChirpStack        | LoRaWAN backend                 |
| Smartsheet        | Task tracking & sprint planning |

---

## 📅 Weekly Progress (Summary)

| Week  | Focus                                 |
| ----- | ------------------------------------- |
| 1     | Soldering connectors, project setup   |
| 2     | Arduino WiFi + LiDAR logger           |
| 3–4   | Outdoor testing + hardware fixes      |
| 5     | RFID integration + dashboard updates  |
| 6     | LiDAR data filtering + timestamping   |
| 7     | Codebase merge to PlatformIO          |
| 8–10  | LoRaWAN research + ChirpStack setup   |
| 11–12 | PCB design + WiFi module installation |

---

## 🧠 Key Learnings

* Embedded C++ for multi-sensor systems
* Hardware-software integration in outdoor field conditions
* PCB prototyping for rapid sensor assembly
* Agile teamwork and modular firmware design
* Web-based UIs for physical systems

---

## 📁 Resources

* 📊 [Smartsheet Dashboards (Internal)]
* 📘 [ChirpStack Docs](https://www.chirpstack.io/)
* 🔗 [RAK3172 Docs](https://docs.rakwireless.com/Product-Categories/WisDuo/RAK3172/)
* 📂 [Google Sheets API](https://developers.google.com/sheets/api)
* 🧰 [PlatformIO Docs](https://docs.platformio.org/)

---

## 📬 Contact

**Author**: *\[Tio Adesanya]*
**Role**: Electrical Engineering Intern – Everzip Project, Summer 2025
**Email**: \[[atioluwanimofe@gmail.com](mailto:atioluwanimofe.com)]
**Portfolio**: \[(http://tioluwanimofe.netlify.app/)]
**LinkedIn**: \[linkedin.com/in/[tioluwanimofe-adesanya/](https://www.linkedin.com/in/tioluwanimofe-adesanya/)]
