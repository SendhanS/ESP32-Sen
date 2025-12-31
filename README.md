# ESP32-Sen
A compact ESP32-S3-MINI-1-N8 development board with USB-C (ESD protected), a 4-layer PCB stack-up (signal / GND / power / signal), and 3.3 V regulation using the TLV75801. Includes GPIO buttons, a WS2812B status LED, and space for an onboard I²C OLED breakout.
The board is intended for learning, experimentation, and portfolio demonstration of embedded systems and PCB design practices.
Status: Not yet tested.
The design is functional in theory but may require revisions and improvements after bring-up.

**Overview**

This board provides a clean ESP32-S3 core with USB-C connectivity, proper ESD protection, a structured 4-layer PCB stack-up, and expansion options for basic UI and peripherals. The goal was to move beyond simple 2-layer hobby boards and design something closer to real-world embedded hardware.

![3D render]ESP32_Sen.png)


**Key Features**

ESP32-S3-MINI-1-N8 module

USB-C connector (USB4105)

Differential USB D+ / D− routing

ESD protection using D3V3XA4B10LP TVS diodes

TLV75801 linear regulator (5 V USB → 3.3 V)

4-layer PCB stack-up:

Top: Signal + components

Inner 1: Solid GND plane

Inner 2: Power plane (3.3 V)

Bottom: Signal routing

WS2812B RGB status LED

BOOT and RESET buttons

Two additional GPIO buttons (GPIO4, GPIO5)

**Power Architecture**

Primary power input via USB-C (5 V)

Onboard TLV75801 LDO generates 3.3 V for ESP32 and peripherals

3.3 V rail is exposed on headers for external devices

Design allows future extension for alternative power input with minor modifications


I²C header and reserved space for a 0.91" OLED display module

GPIO headers for expansion

**USB Design Notes**

USB D+ and D− routed as a differential pair

Length-matched and impedance-aware routing

ESD protection placed close to the USB connector

Intended for USB device mode (programming and serial communication)

**I²C and Display Support**

Dedicated I²C header (3.3 V logic)

PCB space reserved for a common 0.91" 128×32 I²C OLED module

Display is optional and not populated by default

**Known Limitations / Future Improvements**

Board has not been fabricated or tested yet

No battery power or charging circuit

No current measurement or power monitoring

Firmware bring-up examples not included yet

OLED mounting footprint may need adjustment depending on module vendor
