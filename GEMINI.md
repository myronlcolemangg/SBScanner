# Project Overview

This project contains the software for the Scangenie, an ESP32-S3 based barcode scanner. The device features a 1.14" LCD, a barcode/QR code scanner, a Type-C USB port, and a buzzer. The software is developed using the Arduino IDE.

The primary purpose of this project is to provide example code and libraries to interact with the Scangenie hardware. The examples demonstrate how to read barcodes, display them on the screen, and send them to a web server or over Bluetooth.

# Building and Running

To build and run the software on the Scangenie device, you will need to follow these steps:

1.  **Set up the Arduino IDE:**
    *   Download and install the Arduino IDE (version 1.8.19 is recommended).
    *   Add the ESP32 board support by adding the following URL to the "Additional Board Manager URLs" in the Arduino IDE preferences:
        ```
        https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
        ```
    *   Install the "esp32" boards package from the Boards Manager.
    *   Select the "ESP32S3 Dev Module" board in the Arduino IDE.

2.  **Install Libraries:**
    *   Download the `libraries.zip` file from the root of this repository.
    *   Extract the contents and copy them to your Arduino libraries folder (usually `Documents/Arduino/libraries`).
    *   Install the `Adafruit GFX` and `Adafruit ST7789` libraries from the Arduino Library Manager.
    *   If you are using the Bluetooth HID example, install the `ESP32-BLE-Keyboard` library by T-vK from the Arduino Library Manager.

3.  **Upload and Run:**
    *   Open one of the example `.ino` files from the `examples` directory in the Arduino IDE.
    *   Connect the Scangenie to your computer via the "PROG" USB-C port.
    *   Select the correct COM port in the Arduino IDE.
    *   Click the "Upload" button to build and flash the code to the device.

# Development Conventions

*   The project is written in C++ for the Arduino framework.
*   The code is organized into examples, each demonstrating a specific feature of the Scangenie.
*   The `DE2120_Arduino_Library` is used to interface with the barcode scanner module.
*   The `Adafruit_GFX` and `Adafruit_ST7789` libraries are used for the display.
