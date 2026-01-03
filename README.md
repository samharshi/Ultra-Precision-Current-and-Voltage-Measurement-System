# Ultra precision current and voltage measurement system 

🎯 Key Objectives

Measure current from 1 µA to 100 mA with high precision

Measure voltage from 1 V to 12 V accurately

Minimize loading effect on the device under test

Perform real-time data acquisition using an embedded system

Store and monitor measured data via serial communication

⚙️ System Architecture

The system consists of two main sensing subsystems:

Ultra-Precision Current Sensing Circuit

Precision Voltage Sensing Circuit

Measured values are processed by the STM32 microcontroller and transmitted to a PC using UART communication, where data is logged using PuTTY.

🔌 Ultra-Precision Current Sensing Circuit

The current sensing circuit is designed to accurately detect very small currents using a shunt-based measurement technique.

Circuit Description

Uses precision shunt resistors to convert current into a measurable voltage

An operational amplifier (LM358N) is used to amplify the voltage drop across the shunt resistor

Capacitors are included for noise filtering and signal stability

Multiple current ranges are supported using different shunt resistors selected via toggle switches

Current Measurement Ranges
Range Type	Shunt Resistor
Micro-amp range	100 Ω
Milli-amp range	1 Ω
🔋 Precision Voltage Sensing Circuit

The voltage sensing circuit is designed using a resistive voltage divider to scale down the input voltage to a level safe for the STM32 ADC.

Circuit Description

Voltage divider reduces input voltage (1 V – 12 V)

Ensures ADC input remains within allowable limits

High-value resistors are used to reduce loading effect on the DUT

🧠 Microcontroller Unit

Controller: STM32F411

Handles ADC sampling for current and voltage

Performs data processing and scaling

Sends measured values via UART to PC

Designed for real-time and stable operation

🧩 Components Used
Hardware Components

STM32F411 Development Board

ST-Link Debugger

UART TTL Serial Converter

Operational Amplifier (LM358N)

Shunt Resistors

1 Ω (milli-amp range)

100 Ω (micro-amp range)

Capacitors

220 µF

Resistors

1 MΩ

3.3 MΩ

330 Ω

10 Ω

Breadboard

Jumper Wires

3 Toggle Switches

💻 Software & Tools

STM32CubeIDE – Firmware development

PuTTY – Serial communication and data logging

UART Communication – Data transmission from MCU to PC

📊 Data Storage & Visualization

Measured current and voltage values are transmitted via UART

PuTTY is configured to:

Receive serial data

Display real-time measurements

Log data for further analysis

🚀 How to Run the Project

Connect the sensing circuits to the STM32F411 board

Program the microcontroller using STM32CubeIDE

Connect UART TTL converter to the PC

Open PuTTY and configure:

Correct COM port

Baud rate (as defined in firmware)

Power the system and observe real-time measurements

📈 Applications

Low-power electronics testing

Sensor characterization

Precision laboratory measurements

Embedded system measurement platforms
