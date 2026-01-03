# Ultra-Precision Current and Voltage Measurement System

## 📌 Project Overview
This project focuses on designing and implementing an **ultra-precision embedded measurement system** capable of accurately measuring very small **currents** and **voltages** without significantly affecting the **Device Under Test (DUT)**.

The system is built using the **STM32F411 microcontroller**, chosen for its high performance, reliability, and suitability for real-time data acquisition. Measured data is transmitted to a PC using **UART communication** and logged using **PuTTY**.

---

## 🎯 Project Objectives
- Measure current in the range **1 µA to 100 mA**
- Measure voltage in the range **1 V to 12 V**
- Minimize loading effect on the DUT
- Enable real-time data acquisition
- Log measurement data via serial communication

---

## ⚙️ System Architecture
The system consists of:
- Ultra-Precision Current Sensing Circuit
- Precision Voltage Sensing Circuit
- STM32F411 Microcontroller
- UART-based communication for data logging

---

---

## 🔌 Ultra-Precision Current Sensing Circuit
The current sensing circuit uses **precision shunt resistors** to convert current into a small voltage. This voltage is amplified using an **LM358N operational amplifier** before being measured by the STM32 ADC.

### Current Measurement Ranges
| Range | Shunt Resistor |
|------|----------------|
| Micro-amp range | 100 Ω |
| Milli-amp range | 1 Ω |

---

## 🔋 Precision Voltage Sensing Circuit
The voltage sensing circuit is implemented using a **resistive voltage divider** to safely scale voltages from **1 V to 12 V** to a level suitable for the STM32 ADC.

---

## 🧠 Microcontroller Unit
- **Microcontroller:** STM32F411
- Performs ADC sampling
- Processes and scales measurements
- Sends data via UART
- Supports real-time operation

---

## 🧩 Components Used

### Hardware Components
- STM32F411 Development Board  
- ST-Link Debugger  
- UART TTL Serial Converter  
- Operational Amplifier (LM358N)  
- Shunt Resistors  
  - 1 Ω (milli range)  
  - 100 Ω (micro range)  
- Capacitors  
  - 220 µF  
- Resistors  
  - 1 MΩ  
  - 3.3 MΩ  
  - 330 Ω  
  - 10 Ω  
- Breadboard  
- Jumper Wires  
- 3 Toggle Switches  

---

## 💻 Software & Tools
- **STM32CubeIDE** – Firmware development
- **PuTTY** – Serial communication and data logging
- **UART Protocol** – Data transmission

---

## 📊 Data Storage & Logging
- Measurement data is transmitted via UART
- PuTTY is used to:
  - View real-time measurements
  - Store serial data for analysis

---

## 🚀 How to Run the Project
1. Assemble the current and voltage sensing circuits
2. Connect circuits to the STM32F411 board
3. Program the MCU using STM32CubeIDE
4. Connect UART TTL converter to the PC
5. Open PuTTY and configure the correct COM port and baud rate
6. Power the system and observe real-time measurements

---

## 📈 Applications
- Precision laboratory measurements
- Low-power electronics testing
- Sensor characterization
- Embedded measurement systems

---



