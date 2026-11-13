# Signal Scout Hardware

Physical enclosure, 3D print models, and Bill of Materials (BOM) for deploying self-contained, wall-mounted **Signal Scout Watcher** edge sensor nodes.

Designed as an ultra-compact "plug-and-forget" sensor that mounts directly to a standard USB power brick without dangling cords.

---

## Bill of Materials (BOM)

| Component | Description | Link |
| :--- | :--- | :--- |
| **Microcontroller** | Seeed Studio XIAO ESP32 variant (`XIAO ESP32C3`, `XIAO ESP32C5`, `XIAO ESP32C6`, or `XIAO ESP32S3`) | [Seeed Studio](https://www.seeedstudio.com/) |
| **Power Brick** | Low-profile USB-A Wall Charger | Amazon: https://www.amazon.com/dp/B097XM25PL |
| **USB Adapter** | USB-A to USB-C Adapter | Amazon: https://www.amazon.com/dp/B0F7XVL3S7 |
| **Antenna** | Standard Seeed A-01 Wi-Fi/BT Antenna | Seeed Studios: https://www.seeedstudio.com/FPC-Antenna-A-01-for-XIAO-ESP32C3-C5-p-6439.html |

---

## Repository Structure

```text
├── Photos/       # Assembled hardware and build reference photos
├── STEP/         # CAD source files for remixing and modifying
├── STL/          # Ready-to-slice 3D print files
└── README.md
```

---

## 3D Printing Guidelines

* **Recommended Material:** 
  * **PETG** or **ABS/ASA** recommended for outdoor deployments.
  * **PLA** is acceptable for indoor deployments.
* **Layer Height:** `0.20 mm`
* **Infill:** `15% – 20%`, it is mostly walls anyways.
* **Supports:** None required when oriented flat face down. Because the top section is square, bridging is easy. 

---

## Assembly & Deployment

1. **Flash Firmware:** Flash the node using the [Signal-Scout-Watcher](https://github.com/WhatIsInCreedmoor/Signal-Scout-Watcher) firmware and provision your device secrets.
2. **Mount Hardware:**
   * Connect the external 2.4 GHz antenna to the Seeed XIAO IPEX/U.FL connector.
   * Connect the USB-A to USB-C adapter into the power supply.
   * Connect the XIAO device to the USB-A to USB-C adapter in such a way that the antenna is on the same side of the XIAO as the prongs for the power supply
   * Slide the Seeed Studio XIAO board into the 3D-printed case.
   * Slide the case assembly directly onto the USB power brick port.
3. **Deploy:** Plug into any standard AC wall outlet within range of your target monitoring area and Wi-Fi uplink, ideally on a wall facing the area to monitor.

---

## Related Projects

* **[Signal-Scout](https://github.com/WhatIsInCreedmoor/Signal-Scout):** Web backend, ELINT mapping interface, and management server.
* **[Signal-Scout-Watcher](https://github.com/WhatIsInCreedmoor/Signal-Scout-Watcher):** Edge sensor firmware for ESP32-C3, C5, C6, and S3.
