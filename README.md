🔌 ATtiny85 Relay Control System

This is a compact relay control system based on the **ATtiny85 microcontroller**, designed to switch a load based on sensor input, with **OLED display feedback**. It is ideal for low-power embedded automation projects such as smart switching, environment monitoring, or IoT integration.

## 📦 Features

* 🔹 **ATtiny85** MCU-based controller
* 🔹 **Relay Driver Circuit** using optocoupler and NPN transistor
* 🔹 **0.96” I2C OLED display** for real-time status display
* 🔹 **Analog sensor input** (e.g., temperature, LDR, etc.)
* 🔹 **5V regulated power supply** via AMS1117
* 🔹 **Compact 2-layer PCB** layout
* 🔹 **Status LEDs** and programming headers

---

## 🧩 Schematic Overview

The circuit includes:

* ATtiny85 microcontroller (U1)
* AMS1117 5V regulator
* PC817 optocoupler for relay isolation
* NPN transistor (BC547) to drive the relay
* 1 SPDT relay for controlling loads
* OLED display via I2C (SDA/SCL on PB0/PB2)
* Analog sensor interface on PB4
* ISP header for programming the ATtiny85


## 🛠️ Getting Started

### 🔧 Hardware Required

* ATtiny85 microcontroller
* 0.96" OLED display (I2C)
* Relay module (5V SPDT)
* PC817 optocoupler
* BC547 NPN transistor
* AMS1117 5V regulator
* Capacitors (100nF, 22uF)
* Resistors (1kΩ, 10kΩ, etc.)
* LED (optional for status)
* Analog sensor (optional)
* Custom PCB (provided)

### ⚙️ Programming the ATtiny85

You can use an **Arduino as ISP** or **USBtinyISP** to program the ATtiny85. Pin mapping:

| ATtiny85 Pin | Function            |
| ------------ | ------------------- |
| PB0 (pin 5)  | SDA (OLED)          |
| PB1 (pin 6)  | Status LED          |
| PB2 (pin 7)  | SCL (OLED)          |
| PB3 (pin 2)  | Relay driver input  |
| PB4 (pin 3)  | Analog sensor input |
| PB5 (pin 1)  | RESET (ISP)         |

Upload code using Arduino IDE with ATtiny Core installed.

---

## 💡 Example Use Case

This system can:

* Read analog sensor values (e.g., light or temperature)
* Display values on OLED
* Activate a relay based on a threshold value
* Show relay ON/OFF status via LED or OLED


Feel free to reach out or contribute via issues or pull requests!
Let me know if you'd like help creating the Arduino sketch or linking your actual circuit operation logic to the firmware!
