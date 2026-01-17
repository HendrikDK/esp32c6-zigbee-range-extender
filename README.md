# ESP32-C6 Zigbee Range Extender (Router)

This project shows how to use an **ESP32-C6-DevKitC-1U** as a **Zigbee Range Extender (Router)**
using the official **Arduino ESP32 Zigbee** framework.

## Hardware
- ESP32-C6-DevKitC-1U (external antenna required)
- 2.4 GHz u.FL / IPEX antenna (2–3 dBi recommended)
- USB-C data cable
- Zigbee coordinator (Zigbee2MQTT or ZHA)

## Arduino Settings (Important)
- Board: ESP32C6 Dev Module
- USB CDC On Boot: ENABLED
- Zigbee Mode: Zigbee ZCZR (coordinator/router)
- Partition Scheme: Zigbee ZCZR 4MB with spiffs
- Flash Size: 4MB (32Mb)

## Sketch
The Arduino sketch is located here:

The sketch:
- Starts the ESP32-C6 as a Zigbee Router
- Allows up to 20 child devices
- Uses the BOOT button (>3s) for Zigbee factory reset

## Upload
Open the sketch in Arduino IDE and click **Upload**.

If upload gets stuck at "Connecting…":
- Hold BOOT
- Press RESET
- Release RESET
- Release BOOT

## Pairing
Enable **Permit Join** on your Zigbee coordinator and reset the ESP32-C6.
The device will join as a Zigbee Router.

## Result
A stable, mains-powered Zigbee router based on ESP32-C6.