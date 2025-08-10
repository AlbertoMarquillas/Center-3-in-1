# Center-3-in-1
Repurpose a 2015 ASUS ROG laptop into a 3-in-1 home hub: real-time monitoring of local/remote systems, IoT control via MQTT and Node-RED/Home Assistant, and media serving with Jellyfin. Runs on Linux Mint XFCE for stability, low resource usage, and no hardware upgrades.

# ASUS ROG (2015) — 3-in-1 Home Hub

This project repurposes a 2015 ASUS ROG laptop into a **lightweight home server** with three main functions:

1. **Real-time monitoring station**  
   Displays system stats, remote PC metrics, and IoT sensor data using Conky, Glances, and optionally Grafana.

2. **Hardware & IoT control**  
   Acts as a central automation hub with MQTT broker (Mosquitto) and Node-RED/Home Assistant for orchestrating devices.

3. **Media server**  
   Serves multimedia via Jellyfin in direct play mode (no transcoding).

---

## Features
- Runs on **Linux Mint XFCE** for low resource usage and stability.
- **No hardware upgrades** required.
- Remote monitoring of other devices on the network.
- Local IoT control and automation.
- Media streaming within LAN.

---

## Project Structure
- **docs/** — Documentation and setup guides.
- **config/** — Service configurations (Conky, Node-RED, Jellyfin, etc.).
- **scripts/** — Helper scripts for automation and monitoring.
- **data/** — Media library or IoT data storage.

---

## Quick Start
1. Install Linux Mint XFCE on the laptop.
2. Configure:
   - **Conky + Glances** for monitoring.
   - **Mosquitto + Node-RED/Home Assistant** for IoT control.
   - **Jellyfin** for media streaming.
3. Connect via Ethernet for best performance.
4. Enjoy your all-in-one home hub.

---

## License
MIT License
