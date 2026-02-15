# 🏎️ GT7 Shaker - Haptic Feedback & Telemetry Engine

**The most advanced low-latency shaker solution for Gran Turismo 7 on Android. And probaly the only**

![Splash Screen](loadingscreen.png)

## 📋 Overview
**GT7 Shaker is foremost a high-performance haptic feedback (shaker) application**, designed to bring professional-grade immersion to your sim-rig. 

While it includes a secondary, full-featured race dashboard, its core purpose is to translate complex vehicle physics into physical feedback. By using real-time telemetry data, the app generates immersive tactile sensations through your device's audio output, allowing you to "feel" the car and the track.

> ⚠️ **Hardware Requirement:** To use the haptic feedback features, you need a dedicated tactile setup. This app generates audio-based signals that require an external amplifier (e.g., **Nobsound NS-10G**) and haptic feedback transducers/bass shakers (e.g., **Dayton Audio BST-1**) mounted to your racing seat or rig.
---

## ✨ Key Features: The Shaker Engine (Primary)
The heart of this app is a custom-built C++ audio engine that transforms raw telemetry into immersive physics-based feedback with zero perceptible lag.

* **⚡ Suspension & Road Effects:** Feel the texture of the track, every curb strike, and the weight transfer of the car through advanced suspension telemetry.
* **🛞 Traction & Grip Feedback:** Detect tire slip, understeer, and brake lock-ups before they happen, allowing you to react faster and save your tires.
* **🔥 Dynamic Engine Effects:** Immersive engine vibrations that scale with RPM and torque, giving you a better "feel" for your shift points.
* **💥 Collision Impact System:** Directional and intensity-based feedback for impacts with other cars or barriers.
* **🔧 Professional Tuning:** Deep customization with individual sliders to fine-tune intensity and sensitivity for each specific effect, ensuring it matches your specific shaker hardware perfectly.

---

## 📊 Integrated Race Dashboard (Secondary)
When you aren't focusing on the physical feedback, the app provides a crystal-clear visual interface for critical race data:

* **🛞 Live Tire Temperatures:** Visual heat-map for all 4 tires (Cold/Optimal/Hot) to help you manage grip and strategy.
* **⏱️ Advanced Lap Timing:** Integrated lap counter with dynamic pace indicators (Green/Red trend arrows).
* **🏎️ Telemetry Overlays:** Detailed real-time data for RPM, Gear, and Speed.
  
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

## 🔒 Privacy & Permissions

This application is built with a "Privacy by Design" approach. It is a local tool for your sim-rig and does not interact with the cloud.

### Privacy Policy
* **No Data Collection:** This app does not collect, store, or share any personal information, telemetry data, or usage statistics.
* **No Tracking:** There are no analytics, no advertisements, and no third-party trackers included in the code.
* **Offline / Local Only:** All communication happens exclusively between your Android device and your PlayStation on your local home network. No data ever leaves your house.

### Permissions Explained
To provide a zero-latency experience and keep the shaker engine running during long sessions, the following permissions are required:

* **Internet & Network State:** Necessary to receive the high-speed UDP telemetry packets from your PlayStation.
* **WiFi State:** Used to verify that your device is connected to the same network as your console.
* **Foreground Service & Wake Lock:** Ensures that the C++ audio engine and telemetry stream are not interrupted by Android's power-saving features during a race.
* **Modify Audio Settings:** Required to route the haptic feedback signals correctly to your connected amplifier or headphones.
