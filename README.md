<h1 align="center">ESP32S3-Core</h1>

<p align="center">
<a href="README.md">English</a> | <a href="README_zh.md">简体中文</a>
</p>

<p align="center">
Core board based on Espressif ESP32-S3 module
</p>

<p align="center">
Prototype verified, schematic and Gerber files included — ready for PCB fabrication!🚀🚀🚀
If you find it useful, please consider giving it a star!☝️
</p>

## Features

* Dual-layer PCB design
* All GPIOs are fully broken out, with pin layout compatible with Espressif official ESP32-S3 development boards
* Onboard 160×80 resolution LCD display, backlight brightness controlled by `GPIO9`
* Onboard TF (microSD) card slot, sharing the same SPI bus with the LCD
* LCD and TF card are connected to a full-speed SPI bus routed via IOMUX, supporting up to `80 MHz` clock
* Onboard WS2812B RGB LED driven by `GPIO38`
* USB-to-UART bridge: CH340K, supporting baud rates up to `2 Mbps`
* 5V pin supports both input and output; USB Type-C interface protected by a Schottky diode
* Compact form factor, all resistors and capacitors use 0402 packages

## Silkscreen Labels

* `RST` : Reset button
* `BOOT` : Boot mode selection button
* `PWR` : Power indicator LED
* `TX` : UART transmit indicator LED
* `RX` : UART receive indicator LED
* `USB` : USB Type-C port for full-speed USB communication
* `COM` : USB Type-C port for UART flashing and debugging

## Pin Configuration

> Note: The LCD and TF card share the same SPI bus

| Function | Signal     | GPIO |
|----------|------------|------|
| LCD      | LCD_SCLK   | IO12 |
| LCD      | LCD_MOSI   | IO11 |
| LCD      | LCD_CS     | IO10 |
| LCD      | LCD_DC     | IO21 |
| LCD      | LCD_RST    | IO14 |
| LCD      | LCD_BL     | IO9  |
| TF Card  | TF_SCLK    | IO12 |
| TF Card  | TF_MOSI    | IO11 |
| TF Card  | TF_MISO    | IO13 |
| TF Card  | TF_CS      | IO8  |
| UART     | TXD0       | IO43 |
| UART     | RXD0       | IO44 |
| USB      | USB_D-     | IO19 |
| USB      | USB_D+     | IO20 |
| RGB LED  | RGB        | IO38 |

## Hardware Overview

### Board Photo

![Board Photo](image/1.png)

### Schematic

![Schematic](image/2.png)

### PCB Layout

![Top Layer](image/3.png)  
![Bottom Layer](image/4.png)

### 3D Model

![Top View](image/5.png)  
![Bottom View](image/6.png)
