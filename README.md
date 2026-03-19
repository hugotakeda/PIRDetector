-----

# 🛰️ Smart Monitoring System with TTGO T-Camera + Real-Time Notifications

An IoT system developed using the **TTGO T-Camera (ESP32)**, a PIR sensor, and an OLED display. It features motion detection, real-time image capture, and automated alerts sent directly to **Discord**. The project also includes a **Node.js web dashboard** for log visualization, live MJPEG streaming, and visual feedback on the device's display.

> 💡 This project is based on and expanded from: [RobotZero.one - TTGO Security Camera with PIR Motion Sensor](https://robotzero.one/ttgo-security-camera-pir/)

-----

## 🧠 Key Features

  * ✅ **Motion Detection:** High-sensitivity detection using the HC-SR501 PIR sensor.
  * 📸 **Auto Image Capture:** Automatic snapshots via the integrated OV2640 camera.
  * ⏰ **NTP Synchronization:** Precise date/time logging.
  * 💬 **Discord Integration:** Sends instant notifications with the captured image to your server.
  * 🖥️ **Web Dashboard:** Interactive interface to monitor event history.
  * 🌐 **Real-time Communication:** Powered by WebSockets.
  * 📺 **Live Stream:** MJPEG transmission for live viewing via web browser.
  * 🧾 **Local Logging:** Event storage in JSON format.
  * 🧩 **Visual Feedback:** 0.96” OLED display showing system status.

-----

## 🔧 Hardware Components

| Component | Model / Specification |
| :--- | :--- |
| **ESP32 Board** | TTGO T-Camera ESP32 WROVER + Fisheye Lens |
| **Camera** | Integrated OV2640 |
| **Motion Sensor** | PIR (HC-SR501) |
| **Display** | SSD1306 128x64 I2C OLED |
| **Connectivity** | 2.4GHz Wi-Fi |

-----

## 📁 Directory Structure

```text
.
├── arduino/
│   ├── main.ino      # ESP32 Source code
│   └── config.h      # Network and API configurations
├── server/
│   ├── server.js     # Node.js backend
│   ├── index.html    # Frontend Dashboard
│   └── logs.json     # Event database
├── LICENSE           # MIT License
└── README.md
```

-----

## ⚙️ Setup Instructions

### 1\. Hardware Connections (TTGO T-Camera)

| ESP32 Pin | Component Pin |
| :--- | :--- |
| **GPIO33** | PIR Sensor Output |
| **I2C (21/22)** | OLED Display |

### 2\. Arduino Configuration

Open `arduino/main.ino` and update your credentials:

```cpp
const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";
const char* discordWebhook = "YOUR_DISCORD_WEBHOOK_URL";
```

**Compilation Settings:**

  * **Board:** ESP32 Wrover Module
  * **Flash Frequency:** 80MHz
  * **Partition Scheme:** Huge App (3MB No OTA/1MB SPIFFS)
  * **PSRAM:** Enabled

### 3\. Backend Setup (Node.js)

1.  Navigate to the server folder:
    ```bash
    cd server
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the server:
    ```bash
    node server.js
    ```

-----

## 🌐 Accessing the System

  * **Web Dashboard:** `http://localhost:3000`
  * **ESP32 Live Stream:** `http://<ESP32-IP-ADDRESS>`
  * **Notifications:** Check your configured Discord channel.

-----

## 🧪 Future Improvements (To-Do)

  - [ ] Telegram Bot integration.
  - [ ] Basic facial recognition.
  - [ ] Cloud storage (Firebase or Google Drive).
  - [ ] User authentication for the web dashboard.

-----

## 🤝 Contributors

  * **Hugo Takeda** - [GitHub](https://www.google.com/search?q=https://github.com/hugotakeda)
  * **Éden Samuel** - [GitHub](https://github.com/Eden-code01)
  * **Fernando Lopes** - [GitHub](https://github.com/Fernando-Lopes1)

-----

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.
