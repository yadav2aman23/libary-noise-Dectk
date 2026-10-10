# Working Principle

1. **Sound capture:** The INMP441 microphone captures surrounding sound and produces digital audio samples.
2. **I2S transfer:** The microphone sends samples to the ESP32 over the I2S interface.
3. **Audio processing:** Firmware processes the samples and calculates a measurement according to its algorithm.
4. **Wi-Fi connection:** The ESP32 joins the configured wireless network.
5. **Cloud upload:** If Firebase integration is configured in the firmware, the ESP32 sends readings to Firebase Realtime Database.
6. **Monitoring:** Stored readings can be retrieved by a dashboard or another client if one has been built.

## Important measurement note

The result should not be called an accurate dB value unless the microphone and processing chain have been calibrated and validated. Otherwise, describe it as a relative noise level or processed microphone reading.

## Data flow

`INMP441 microphone → I2S → ESP32 → Wi-Fi → Firebase Realtime Database → Dashboard (optional)`
