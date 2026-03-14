Smart Traffic Light System with Emergency Vehicle Priority

> An IoT-based smart traffic management system that detects emergency vehicle sirens and dynamically adjusts traffic signals to ensure faster emergency response.

Overview

Traditional traffic lights operate on fixed cycles — they can't react to emergency vehicles. This project solves that by using **LM393 sound sensors** and an **Arduino microcontroller** to detect emergency sirens and immediately grant a green signal to the affected lane.

Built as part of BScIT final year project at **Bhaskar Waman Thakur College of Science** (**Viva College, Virar West**) , Mumbai University.

**Department:** Information Technology

How It Works

1. All 4 lanes cycle normally — each gets a **green light for 5 seconds**
2. LM393 sound sensors continuously listen for siren frequencies
3. If a siren is detected (**400–1600 Hz**, **≥ 45 dB**):
   - The emergency lane gets **green for 15 seconds**
   - All other lanes turn **red**
4. After the vehicle passes, the system **resumes normal operation**

Hardware Components

Component 

1. Arduino Microcontroller :- Brain of the system — processes sensor data 
2. LM393 Sound Sensors (×4) :- Detects emergency siren frequency & decibels 
3. LED Traffic Lights (×4 lanes) :- Red/Green LEDs for signal display 
4. Power Supply Unit :- Stable power for uninterrupted operation

Software & Code

Three versions of the Arduino code and pin connections are included in the project report:

 **Basic Version** — Simple 5-second cyclic traffic loop
 **Improved Version** — Adds FFT-based siren detection using **arduinoFFT** library
 **Final Version** — Can override signals and Adds 45 dB threshold filtering to reduce false triggers

Detection Parameters: 
- Frequency range: **400 Hz – 1600 Hz**
- Minimum decibel level: **≥ 45 dB**
- Normal green duration: **5 seconds**
- Emergency green duration: **15 seconds**

 Testing Results

| Test | Result |
|------|--------|
| Normal traffic light cycle | ✅ Pass |
| Emergency siren detection | ✅ Pass |
| Background noise filtering | ✅ Pass |
| Multiple sirens handling | ✅ Pass |

System accuracy: **>90%** under simulated conditions.

 Future Scope

- **AI-based sound classification** — better siren vs noise differentiation
- **Vehicle-to-Infrastructure (V2I)** — direct GPS/RFID communication
- **Image processing** — real-time traffic density analysis
- **Cloud dashboard** — centralized monitoring for smart cities

---

 Project Report

Full project documentation (including circuit diagrams, flowcharts, schematic diagrams, and code) is available in **traffic_black_book.docx**


 Author

**Shantanu Kalambe**
- 🎮 [itch.io](https://shantanu-kalambe.itch.io)
- 🐙 [GitHub](https://github.com/shantanukalambe77)
- 📍 Virar, Maharashtra, India

License

This project is submitted as an academic project at Mumbai University. All rights reserved © 2024 Shantanu Kalambe.
## 📄 License

This project is submitted as an academic project at Mumbai University. All rights reserved © 2024 Shantanu Kalambe.
