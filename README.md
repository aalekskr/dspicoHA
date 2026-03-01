# dsPico Home Assistant Interface
**Status: Phase 1 (Architectural Design & Hardware Prototyping)**

A project to repurpose a Nintendo DS as a dedicated Smart Home Dashboard using an RP2040-based flashcard and an ESP32-C3 for Wi-Fi connectivity.

## System Architecture
The project uses a three-tier hardware stack to bridge legacy gaming hardware with modern IoT APIs:

1. **Nintendo DS (Frontend):** UI developed in **C** using the `libnds` library. Handles touch input and data visualization.
2. **RP2040 (Bridge):** Acts as the interface between the DS Slot-1 bus and the network module.
3. **ESP32-C3 (Network):** Handles WPA3 Wi-Fi connectivity and fetches JSON data from the **Home Assistant REST API**.



## Tech Stack
* **Languages:** C (libnds, Pico SDK), C++ (Arduino/ESP-IDF)
* **Communication:** UART (Serial) at 115200 baud
* **Hardware:** Nintendo DS Lite, dsPico (RP2040), ESP32-C3 SuperMini

## Roadmap
- [x] Hardware Selection & Architecture Design
- [ ] Hello World on DS via dsPico
- [ ] UART Communication bridge between ESP32 and RP2040
- [ ] Home Assistant API Integration