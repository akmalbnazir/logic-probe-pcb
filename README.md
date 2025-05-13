# 🧠 Logic Probe Tool (USB-Powered)

A simple but powerful **USB-powered logic probe** built in **KiCad**. This compact tool visually detects whether a digital signal is **HIGH** or **LOW** using two LEDs — great for debugging microcontroller pins, communication lines, or basic digital logic gates.

---

## 🔌 Features

- ✅ **USB-C powered** — no external batteries
- 🔴 **Red LED** lights when signal is LOW
- 🟢 **Green LED** lights when signal is HIGH
- 🔁 Built with a **74HC14 Schmitt Trigger inverter**
- 🔥 Protected by a **PTC resettable fuse** and **Schottky diode**
- 🧪 **Voltage divider** ensures safe signal detection
- 🛡️ Ground-referenced probe tip with pull-down resistor
- 💡 Fits on a small 2-layer PCB, ideal for hand-soldering

---

## 📐 Schematic Overview

The probe input passes through two inverters on a 74HC14 IC:
- One output drives the **RED LED** (LOW indicator)
- The other drives the **GREEN LED** (HIGH indicator)

Power comes from USB-C and is protected with:
- A **Schottky diode** for reverse polarity
- A **PTC fuse** for overcurrent protection
- **Bypass capacitors** for stable voltage

---

## 🧰 BOM (Bill of Materials)

| Component     | Value/Part             |
|---------------|------------------------|
| USB Connector | USB_C_Receptacle_USB2.0_16P |
| U1            | 74HC14 Schmitt Inverter |
| F1            | Polyfuse 500mA         |
| D1            | Schottky Diode (e.g., SS14) |
| R1            | 10kΩ pull-down         |
| R2, R3        | 220Ω LED current limit |
| D2            | Red LED                |
| D3            | Green LED              |
| C1, C2        | 0.1 µF & 10 µF ceramic capacitors |
| J2            | Probe input pin header |
| GND Pad       | Ground contact pad     |

---

## 🧠 Usage

1. Plug the logic probe into a USB-C power source.
2. Touch the **probe pin** to any digital signal line (3.3V or 5V logic).
3. Observe:
   - 🔴 Red LED = LOW (0V)
   - 🟢 Green LED = HIGH (3.3V/5V)
4. The pull-down resistor ensures stable readings even on floating lines.

---

## 📸 Preview
![image](https://github.com/user-attachments/assets/5da816d0-202a-4e9c-9f05-d5a092993e38)

---

## 🛠 Files Included

- `logic-probe.kicad_pro` — project file
- `logic-probe.kicad_sch` — schematic
- `logic-probe.kicad_pcb` — PCB layout
- `gerbers/` — ready-to-manufacture fabrication files
- `README.md` — this documentation

---

## 📜 License

MIT License — free to use, modify, and distribute. Give credit if you build on this work.

---

## 👨‍💻 Author

Designed by Akmal Nazir – May 2025  
KiCad-powered, beginner-friendly, proudly hand-soldered.
