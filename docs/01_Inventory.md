# Phase 0 — Inventory (Windows Version)

Goal: collect all technical details of the ASUS ROG (2015) laptop before installing and configuring the 3-in-1 Home Hub, using Windows tools.

---

## Data to collect

1. **Exact model**
   *Example:* ASUS ROG GL552VW
   **Windows command:** Press `Win + R` → type `msinfo32` → check **System Model**.

2. **Processor (CPU)**
   *Example:* Intel i7-4720HQ, 4 cores/8 threads, 2.6 GHz
   **Windows command:** In `msinfo32`, check **Processor**.

3. **Total RAM**
   *Example:* 8 GB DDR3
   **Windows command:** In `msinfo32`, check **Installed Physical Memory (RAM)**.

4. **Storage**
   Type (HDD/SSD) and capacity
   **Windows command:** Open PowerShell and run:

   ```powershell
   Get-PhysicalDisk | Format-Table FriendlyName,Size,MediaType
   ```

5. **Graphics card**
   Integrated or dedicated (NVIDIA/AMD)
   **Windows command:** Press `Win + R` → type `dxdiag` → go to the **Display** tab.

6. **Available ports**
   USB (2.0/3.0), HDMI, Ethernet, SD card reader, etc. (check physically).

7. **Battery health** (optional)
   *Example:* OK, not charging, swollen
   **Windows command:** Open PowerShell and run:

   ```powershell
   powercfg /batteryreport
   ```

   This generates an HTML report in your user folder.

8. **Connectivity**
   Is Ethernet functional? Is Wi-Fi stable? Test both.

9. **BIOS version** (optional)
   **Windows command:** In `msinfo32`, check **BIOS Version/Date**.

---

## Collected specifications

* **Exact model:** ASUS ROG GL752VW
* **CPU:** Intel® Core™ i7-6700HQ CPU @ 2.60 GHz (4 cores / 8 threads)
* **RAM:**  8 GB DDR4 (7.90 GB usable)
* **Storage:** 1 TB HDD — HGST HTS721010A9E630
* **GPU:** NVIDIA GeForce GTX 960M, 2 GB VRAM (2010 MB) + 4 GB shared memory (total ~6 GB)
* **Ports:** Power input, Mini DisplayPort, HDMI, 1 × USB 3.0 (left), Ethernet (RJ-45), 1 × USB 3.0 (left), USB-C, 2 × USB 2.0 (right), 2 × 3.5 mm audio jacks (headphone & microphone), DVD optical drive, Kensington lock slot
* **Battery:** Li-ion, design capacity 48,240 mWh, full charge capacity 30,585 mWh, 164 cycles (~63% of original capacity)
* **Connectivity:** Ethernet port + Wi-Fi
* **BIOS version:** GL752VW.214 — 18/04/2016

---
