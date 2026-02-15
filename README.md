# 🏎️ GT7 Shaker - Realtime Telemetry Dashboard

**Transform your Android device into a professional racing dashboard for Gran Turismo 7.**

![Splash Screen](loadingscreen.png)

## 📋 Overview
GT7 Shaker is a lightweight, zero-latency telemetry dashboard designed for Sim Racers. It connects directly to your PlayStation 4 or 5 via UDP to display critical race data that isn't always visible on the main screen.

**🚀 Evolution:** This Android application is a direct evolution and mobile port of my open-source project, **[GT7 Shaker for Linux](https://github.com/Helskov/GT7-Shaker-for-linux)**. It brings the same precision and speed to your phone or tablet.

## ✨ Key Features

* **🛞 Live Tire Temperatures:** Visual heat-map for all 4 tires (Cold/Optimal/Hot) to help you manage grip.
* **⏱️ Advanced Lap Timing:** Integrated lap counter and pace indicators.
* **🔧 Deep Customization:** Fine-tune collision sensitivity and shaker intensity.
* **⚡ Zero Lag:** Uses native UDP packets for instant feedback.
  
## 🔊 High-Performance Audio Engine
GT7 Shaker isn't just a visual tool. It features a custom-built, low-latency audio engine designed for haptic feedback and real-time sound generation:

* **Native C++ Integration:** Uses a compiled `libnative_audio.so` library to bypass standard Android audio latency, ensuring your shakers react instantly to in-game events.
* **Advanced Java Bridge:** Leverages a dedicated Java-based `AudioGenerator` for seamless communication between the telemetry data and the hardware.
* **Dedicated Background Service:** Powered by a separate Android service, the audio engine continues to run flawlessly even if you switch apps or turn off the screen during long endurance races.

---

## 📸 Screenshots

### Race Dashboards
| Standard Dash | Telemetry Focus |
|:---:|:---:|
| ![Standard Dash](Racedash.png) | ![Telemetry Dash](racedashTelemetry.png) |

### Vehicle & Tire Data
| Tire Temperatures | Initial Connection |
|:---:|:---:|
| ![Tire Temps](tires.png) | ![First Screen](firstscreen.png) |

### Configuration & Settings
| General Settings | Car Profiles | Collision/Shaker |
|:---:|:---:|:---:|
| ![General](generel.png) | ![Profiles](profiles.png) | ![Collision](collision.png) |

---

## 📥 Installation (Android)

Since this app is built by a solo developer and not hosted on the Google Play Store, Android requires a few extra steps to ensure a successful installation.

1.  **Download:** Go to the **[Releases](../../releases)** page and download the latest `.apk` file (e.g., `app-1.4-arm64-v8a-release.apk`).
2.  **Open File:** Once downloaded, open the file from your browser or file manager.
3.  **System Permission:** If prompted that your phone "is not allowed to install unknown apps from this source":
    * Click **Settings** in the popup.
    * Toggle **"Allow from this source"** to ON.
    * Press back and click **Install**.
4.  **Play Protect Warning:** You will likely see a second popup saying **"Blocked by Play Protect"**:
    * Click **"More Details"** (the small arrow down).
    * Select **"Install Anyway"**.
5.  **Launch:** Find **GT7 Shaker** in your app drawer and you're ready to race!

---

## ⚙️ Setup Guide

1.  **Find your PlayStation IP:** On your PS4/PS5, go to **Settings** -> **Network** -> **View Connection Status** and note down the IP address (e.g., `192.168.1.50`).
2.  **Connect the App:** Open **GT7 Shaker** on your phone.
3.  **Enter IP:** Type your PlayStation's IP address into the app's connection screen.
4.  **Race:** The dashboard and shaker engine will activate automatically as soon as you enter a track.

### 2. Connect the App
1.  Ensure your Phone and PlayStation are on the **same Wi-Fi network**.
2.  Enter your PlayStation's IP Address in the app settings.
3.  **Pro Tip:** For the best stability, use a **5GHz Wi-Fi** connection and avoid using Bluetooth peripherals simultaneously unless they support **Bluetooth 5.2+ Low Latency**.

---

## 📜 License & Credits
* This project is based on the original work found at [GT7-Shaker-for-linux](https://github.com/Helskov/GT7-Shaker-for-linux).
* This project is not affiliated with Polyphony Digital or Sony Interactive Entertainment.
* Created by Helskov.
