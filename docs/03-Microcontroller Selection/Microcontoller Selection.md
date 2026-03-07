---
title: Microcontroller Selection
---

This page describes the selection of the microcontroller used in the sensing module. It outlines why the PIC18F47K42 was chosen, the communication required and the necessary pins.

## Selected Microcontoller

Microcontroller: ESP32-S3-WROOM-1-N4

The ESP32-S3-WROOM-1-N4 was selected as the final microcontroller for this sensing subsystem because it provides the communication features, processing capability, and flexibility.

The ESP32-S3 provides:

- Built in I2C support for reading distance data from the distance sensor.
- Multiple UART modules for sending distance and status data to the motor module.
- Alot GPIO pins for sensor control and status LEDs.
- Reliable operation at 3.3V.
- Integrated USB support for programming and debugging.

## ESP32 Table of Contents

| ESP Info | Answer |
|---|---|
| ESP32-S3-WROOM-1-N4 | [Product Link](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639?s=N4IgTCBcDaIIwE4BsBWAtAUQMoAUDMYaWeaA6gEoDylAsmnGgHIAsAwgCpMAiIAugL5A) |
| Datasheet | [ESP32-S3-WROOM-1 Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf) |
| Vendor | [Espressif Systems](https://www.espressif.com/) |
| Unit cost | About $5.06/each |
| Supply Voltage Range | 3.0 V ~ 3.6 V |
| Absolute Maximum current | 355 mA |
| Maximum GPIO current (per pin) | 40 mA |
| Supports External Interrupts? | Yes |
| Programming Hardware | Micro-USB |

## Pin layout for ESP32

| Module | # Available | Needed | Associated Pins |
|---|---:|---:|---|
| UART | 3 | 1 | GPIO16 and GPIO17 |
| I2C | 2 | 1 | GPIO8 and GPIO9 |
| GPIO | 36 | 8 | 3 LED pins and 5 Headers |
| USB Programmer | 1 | 1 | GPIO19 and GPIO20 |

### Communication to the Motor Module

### Communication to the Motor Module

- This sensing module reads the distance value from the distance sensor using I2C through the ESP32.

- The ESP32 processes the distance data and sends the information to the motor control module through UART.

- The motor module determines how to respond based on the received distance data, including slowing down, stopping, or knowing its clear to avoid obstacles.





