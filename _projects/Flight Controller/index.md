---
layout: post
title: Custom Flight Controller
description: Designed and implemented a custom STM32-based flight controller and telemetry system from the ground up, covering hardware integration, low-level firmware, and full system bring-up.
skills:
  - Sensor driver development (I²C/SPI)
  - Real-time systems and hardware timers
  - LORA protocol integration
  - Protoype assembly and validation

main-image: /fc.jpg
---

I architected the complete avionics stack and selected all onboard subsystems, including MCU, IMU, GPS, LoRa radio, SD storage, RTC, ELRS receiver, and servo outputs, defining the electrical interfaces and communication topology between devices.

I implemented all peripheral drivers at register level without vendor libraries, including the 10DoF IMU over I²C, SPI-based LoRa and SD card interfaces, and deterministic PWM generation using hardware timers for four control surfaces. I configured GPS module to output UBX binary packets at controlled update rates and integrated CRSF telemetry.

I assembled and soldered the hardware, performed full system bring-up, validated bus integrity, and tested telemetry logging, sensor acquisition, and actuator control under real operating conditions. The platform executed stable control and logging on a fin-based ground rig.

---

# Specs
- 10DoF IMU (custom driver, no libraries)
- LoRa telemetry link
- SD card flight-data logging
- GPS with UBX binary protocol
- ExpressLRS receiver (CRSF)
- 4× hardware-timer servo outputs
- RTC-backed timestamping

{% include image-gallery.html images="image.png" height="400" %}

