# ESP32 Library Noise Monitor

An IoT project concept for monitoring library sound levels using an ESP32, an INMP441 I2S digital microphone, and Firebase Realtime Database.

> **Important:** Check all GPIO assignments and Firebase features against your actual `.ino` sketch before publishing. This repository template does not claim that every suggested feature is already implemented.

## Features

- Sound sampling using an INMP441 digital microphone
- ESP32-based audio processing
- Wi-Fi connectivity
- Firebase Realtime Database integration (when configured in the firmware)
- Documentation for wiring, working principle, and setup

## Hardware

- ESP32 development board
- INMP441 I2S microphone module
- USB cable and jumper wires
- Wi-Fi network

## Wiring

The following is an **example wiring map only**. Confirm the GPIOs in your firmware before connecting the hardware.

| INMP441 pin | Example ESP32 connection | Purpose |
|---|---|---|
| VDD | 3V3 | Microphone power |
| GND | GND | Common ground |
| SCK / BCLK | GPIO 26* | I2S bit clock |
| WS / LRC | GPIO 25* | I2S word-select clock |
| SD | GPIO 33* | Digital audio output |
| L/R | GND | Select left channel on typical modules |

`*` Example GPIOs only. Your code may use different pins.

See [`docs/wiring-diagram.svg`](docs/wiring-diagram.svg).

## Repository structure

```text
ESP32-Library-Noise-Monitor/
├── firmware/
│   └── README.md
├── docs/
│   ├── wiring-diagram.svg
│   ├── working-principle.md
│   └── firebase-setup.md
├── images/
│   └── README.md
├── .gitignore
├── LICENSE
└── README.md
```

## Setup

1. Install Arduino IDE and the ESP32 board support package.
2. Copy your project sketch into `firmware/` (for example, `ESP32_Library_Noise_Monitor_FIXED.ino`).
3. Open the sketch in Arduino IDE.
4. Install the libraries required by the sketch.
5. Verify the microphone GPIO assignments against the wiring.
6. Configure Wi-Fi and Firebase credentials locally.
7. Select the correct ESP32 board and port, then upload the sketch.
8. Open Serial Monitor and verify device, Wi-Fi, microphone, and database status.

## Firebase and credentials

Never publish Wi-Fi passwords, private keys, service-account files, access tokens, or other secrets. Use placeholders in documentation and review the sketch before pushing it to a public repository. Configure Firebase Authentication and restrictive Realtime Database Security Rules for your use case.

## Measurement note

A value calculated from microphone samples is not automatically a calibrated sound-pressure level in decibels (dB). Accurate dB readings require suitable calibration and a validated measurement method. Describe uncalibrated readings as relative noise level or raw/processed readings.

## Testing checklist

- [ ] ESP32 powers on and appears in Serial Monitor
- [ ] Microphone I2S data is received
- [ ] Wi-Fi connects successfully
- [ ] Firebase writes succeed, if enabled in the sketch
- [ ] Readings respond to changes in the sound environment
- [ ] No credentials or secrets are committed

## Future improvements

- Timestamped reading history
- Noise-threshold alerts
- Multiple monitoring locations
- Historical charts and CSV export
- A mobile-friendly dashboard
- Calibrated sound-level measurement

## License

This template includes an MIT License. Review and update the copyright holder before publishing.
