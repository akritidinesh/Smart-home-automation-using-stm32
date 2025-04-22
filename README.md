🏠 Smart Home Automation System using STM32 and FreeRTOS

This project implements a Smart Home Automation System using an STM32 microcontroller integrated with various sensors and managed by FreeRTOS for efficient multitasking. The system automates common household functionalities such as fan control, lighting, and obstacle detection.

Features
DHT20 Sensor: Monitors temperature and humidity to automate fan control.

LDR (Light Dependent Resistor): Detects ambient light to automatically switch on the light in low-light conditions.

Ultrasonic Sensor: Detects obstacles to enable basic intrusion or object detection.

FreeRTOS: Used for task management to handle sensor readings and actions concurrently.

🛠️ Hardware Used
STM32F4 Series Microcontroller (e.g., STM32F407VET6 / STM32F446RE)

DHT20 Sensor (I2C)

LDR Sensor (Analog input via ADC)

Ultrasonic Sensor (HC-SR04)

Fan (Represented via GPIO controlled output or relay)

Light (LED or Relay output)

ST-Link V2 (for programming/debugging)

📋 Tasks Overview

Task	Functionality	Priority
DHT20 Task :	Reads temperature & humidity, controls fan, Priority :	Medium
LDR Task :	Reads light level, controls light, Priority :	Low
Ultrasonic Task	: Detects obstacles, Priority : 	High

🔄 How it Works
If temperature/humidity exceeds a set threshold, the fan is turned ON.

If ambient light drops below a threshold, the light is turned ON.

If the ultrasonic sensor detects an object within a defined range, it triggers an alert or action.
