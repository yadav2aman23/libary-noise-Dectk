# libary-noise-Dectk





## 🔄 Working Principle

The ESP32 Library Noise Monitor operates through the following steps:

1. **Sound Capture:** The INMP441 microphone detects surrounding sound and generates digital audio samples.
2. **Data Transfer:** The microphone sends audio samples to the ESP32 using the I2S communication protocol.
3. **Noise Calculation:** The ESP32 processes the samples and calculates a sound-level measurement based on the firmware's algorithm.
4. **Internet Connectivity:** The ESP32 connects to a Wi-Fi network.
5. **Cloud Data Upload:** The ESP32 sends the calculated readings to Firebase Realtime Database.
6. **Data Monitoring:** The stored readings can be viewed or used by a connected dashboard to monitor library noise conditions.

### 📌 Important Note

The calculated value should not automatically be considered an accurate sound-pressure level in decibels (dB). Accurate dB measurements require appropriate calibration. The displayed value depends on the microphone, audio-processing algorithm, and firmware configuration.

### 🎯 Project Objective

The main objective of this project is to develop an IoT-based system that helps monitor noise conditions in a library, supports a quieter study environment, and enables remote access to collected noise data.
