# ALC-Guard

**Coursework for DESE71003 - Sensing and IoT**
**Author:** Jingyang Liu | **CID:** 02252219

---

## Project Overview
ALC-Guard is an IoT smart cup system designed to track alcohol intake and provide real-time risk awareness. It uses sensor fusion (Weight, Tilt, Temperature, Gas) to distinguish between drinking, sipping, refilling, and pouring out, helping users monitor their habits via a web dashboard and physical LED feedback.

## Key Features
* **Smart Detection:** Automatically identifies **Drink**, **Small Sip**, **Refill**, and **Pour Out** events.
* **Alcohol Validation:** Filters out non-alcoholic drinks (Water vs. Alcohol) using an MQ-3 sensor.
* **Dual Feedback:**
    * **Cup:** LED flashes (Blue=Water, Red=Alcohol). Solid Red when daily limit exceeded.
    * **Web:** Real-time dashboard with Risk Banner (Units/hr) and Progress Bar (Volume).
* **Night Mode:** Suppresses LED alerts during sleep hours (e.g., 22:00 - 08:00).

## File Structure
```text
ALC-Guard/
├── app.py              # Flask Backend (Runs local server)
├── requirements.txt    # Python dependencies
├── index.html          # Web Dashboard UI
├── events.csv          # Data storage (Auto-generated)
├── Final.ino           # ESP32 Firmware
└── README.md           # This file
