# Project: ASUS ROG (2015) — 3-in-1 Home Hub

**Combined functions:** Monitoring station + IoT/Hardware control + Media server.  
**No hardware upgrades** — designed for low power usage and stability.

---

## Objective
Repurpose an old ASUS ROG (2015) laptop to:
1. Display real-time local and remote system metrics.
2. Control and automate devices (Arduino/ESP32, etc.).
3. Serve a multimedia library over the local network without transcoding.

---

## Scope
- **Recommended OS:** Lightweight Linux (Mint XFCE or Debian + XFCE).
- **Services on the laptop:**
  - **Monitoring:** Conky (desktop) + Glances (API server) and/or Grafana.
  - **IoT automation:** Mosquitto (MQTT) + Node-RED or Home Assistant.
  - **Media:** Jellyfin in **direct play** mode.
  - **File sharing:** Samba (optional).
- **Agents on other devices:**
  - Main PC: Glances/Netdata/script to expose metrics.

---

## Constraints and Assumptions
- No internal hardware changes (no SSD/RAM upgrade).
- Avoid heavy workloads (no video transcoding).
- Ethernet connection recommended for stability.
- Lid open or adequate cooling if running for long periods.

---

## High-Level Architecture
- **Data layer:** Glances on laptop + (optional) InfluxDB/Prometheus.
- **Display:** Conky on screen; optional Grafana in kiosk mode.
- **IoT:** Mosquitto (MQTT) as message bus; Node-RED for logic; USB/Wi-Fi for hardware.
- **Media:** Jellyfin serving files from internal/USB drive.

---

## Deliverables
- Laptop configured to:
  - Auto-start all services.
  - Show a real-time dashboard (Conky or Grafana in kiosk mode).
  - Provide Jellyfin access in LAN.
  - Run MQTT broker and Node-RED ready for IoT.
- Short documentation: IP/ports, credentials, data paths.

---

## Phases

### **Phase 0 — Inventory (10 min)**
Record: exact model, CPU, RAM, storage, battery, USB ports, Ethernet, BIOS version.

### **Phase 1 — Base system (45–60 min)**
Install Linux Mint XFCE, create user, update, enable auto-login, configure power settings, install `ufw`.

### **Phase 2 — Network & usability (20–30 min)**
Set static IP, hostname (e.g., `rog-hub`), optional Samba share, enable SSH keys.

### **Phase 3 — Monitoring (30–60 min)**
Install Conky + Glances, set Conky to autostart.  
(Optional) Install Grafana + InfluxDB/Prometheus.

### **Phase 4 — Media server (30–45 min)**
Install Jellyfin, create library, disable transcoding, test direct play.

### **Phase 5 — IoT/Automation (45–90 min)**
Install Mosquitto + Node-RED (or Home Assistant), create first MQTT flow.

### **Phase 6 — Remote metrics integration (30–45 min)**
Install agent on main PC, display metrics in Conky or Grafana.

### **Phase 7 — Hardening & maintenance (20–40 min)**
Backup configs, minimal `ufw` rules, non-intrusive updates, systemd auto-restart.

---

## Success Criteria
- Laptop screen shows CPU/RAM/network + IoT metrics + main PC status.
- Media plays smoothly in LAN (direct play).
- IoT dashboard accessible from mobile for device control.
- Full auto-recovery after reboot.

---

## Risks & Mitigation
- **Slow/hot:** Native services, no heavy containers, no transcoding.
- **Network issues:** Static IP, cable connection, auto-restart services.
- **Low disk space:** Use external USB drive for media.

---

## Default Setup
- **OS:** Linux Mint XFCE.
- **Dashboard:** Conky (lightweight).
- **Extra metrics:** Glances server; optional Grafana.
- **IoT:** Mosquitto + Node-RED.
- **Media:** Jellyfin (direct play).
