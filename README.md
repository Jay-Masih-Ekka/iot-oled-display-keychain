# ESP32-C3 OLED Video Keychain

This repository contains the C++ source code for a compact, wearable video keychain built using an ESP32-C3 microcontroller and a 1.3-inch I2C OLED display.

## Demo


https://github.com/user-attachments/assets/01cfcb70-f37d-426a-8e7e-f0054f875be1



## Hardware Components & Pinout
* **Microcontroller:** ESP32-C3
* **Display:** 1.3" OLED Display (I2C)

| OLED Pin | ESP32-C3 Pin |
| :--- | :--- |
| **SDA** | GPIO 8 |
| **SCK / SCL** | GPIO 9 |
| **VCC** | 3.3V |
| **GND** | GND |

## Performance Optimizations
Rendering video on an I2C OLED requires overcoming data transfer bottlenecks. This project implements:
* **I2C Fast Mode:** Increased the I2C bus frequency to 400kHz to stabilize the frame rate and prevent choppy video rendering.
* **Optimized Frame Buffering:** Efficiently stores and pushes image arrays to the display to maintain a continuous, smooth video loop.
