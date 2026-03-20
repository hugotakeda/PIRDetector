# PIRDetector

**Intelligent IoT Motion Detection with Discord Integration.**  

A minimalist security solution that utilizes a PIR sensor and an ESP32/Raspberry Pi to detect motion, capture real-time images, and send instant alerts via Discord Webhooks.

## Technical Stack

| Category | Technology |
|---|---|
| **Hardware** | ESP32 / Raspberry Pi + PIR Sensor + Logitech C920 |
| **Backend** | Python (Flask) |
| **Integration** | Discord Webhooks |
| **Processing** | OpenCV |

## Key Features

- **Real-time Detection:** Immediate response to physical motion via PIR sensor.
- **Automated Capture:** High-definition snapshots captured upon detection.
- **Discord Alerts:** Instant notifications including time, location, and snapshot.
- **Web Dashboard:** Minimalist interface for viewing logs and captured photos.

## System Components

- `Arduino/`: Firmware for the motion detection trigger.
- `Servidor/server.py`: Flask-based processing engine and Discord bridge.
- `Servidor/index.html`: Web interface for monitoring.

## Getting Started

1. **Setup:** Configure your `DISCORD_WEBHOOK` in `server.py`.
2. **Installation:** `pip install Flask requests opencv-python Pillow`.
3. **Execution:** Run `python server.py` to start the monitoring bridge.
4. **Hardware:** Connect your PIR sensor to the designated GPIO pin (default: 33).

---

[MIT](./LICENSE) © 2025 hugotakeda
