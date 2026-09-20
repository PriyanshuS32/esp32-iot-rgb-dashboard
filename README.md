# ESP32 IoT RGB LED Web Dashboard

A wireless IoT project that turns an ESP32 development board into a local web server, allowing you to control a 4-pin RGB LED directly from your smartphone or laptop browser over Wi-Fi.

## Features
- **Wireless Control:** Hosts a responsive local HTML web page over Wi-Fi.
- **HTTP Routing:** Changes LED states dynamically using simple HTTP GET requests (`/color/red`, `/color/green`, etc.).
- **Multi-Color Support:** Switch between Red, Green, Blue, Purple, or turn it completely Off.

---

## Wiring Guide

| RGB LED Pin | ESP32 Board Pin | Notes |
| :--- | :--- | :--- |
| **Common Cathode (Longest Pin)** | `GND` | Shared ground |
| **Red Pin** | `D23` (GPIO 23) | Connected via a 220Ω resistor |
| **Green Pin** | `D22` (GPIO 22) | Connected via a 220Ω resistor |
| **Blue Pin** | `D21` (GPIO 21) | Connected via a 220Ω resistor |

---

## Prerequisites
1. **Arduino IDE** installed on your computer.
2. The **ESP32 Board Package** installed via the Arduino Boards Manager.

---

## How to Run

1. Clone or download this repository.
2. Open the `.ino` file in the Arduino IDE.
3. Update the Wi-Fi credentials in the code with your own network details:
   ```cpp
   const char* ssid = "YOUR_WIFI_SSID";
   const char* password = "YOUR_WIFI_PASSWORD";
