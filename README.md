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


