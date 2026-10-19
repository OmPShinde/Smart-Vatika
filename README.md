# Smart Vatika: Smart Plant Monitoring System (Raspberry Pi)

Second-year mini project (SY Sem-IV, Mini Project II) in Electronics and Telecommunication Engineering at Pillai College of Engineering (Autonomous), University of Mumbai, A.Y. 2024-25.

Smart Vatika is a Raspberry Pi 4 based system that monitors soil moisture, light intensity, temperature and humidity, and gives real-time visual and audio feedback, including emoji-based alerts, so that anyone can tell at a glance what a plant needs.

## Project Details

| Field      | Details                                                |
|------------|--------------------------------------------------------|
| Course     | SY Sem-IV, Mini Project II                             |
| Department | Electronics and Telecommunication Engineering          |
| College    | Pillai College of Engineering, University of Mumbai    |
| Year       | A.Y. 2024-25                                           |
| Guide      | Prof. Ishmeet Singh Riar                               |
| Group Code | B1 2                                                   |

## Team

| Roll No. | Name                   |
|----------|------------------------|
| 405      | Nupoor Mangesh Marathe |
| 411      | Manasvi Vivek More     |
| 412      | Aditi Uttam Muni       |
| 413      | Siddhi Sanjay Naik     |
| 416      | Om Prakash Shinde      |

## Problem Statement

Plant care depends on consistent monitoring of soil moisture and light. Manual methods lead to overwatering, underwatering and poor lighting, and the lack of real-time feedback makes the process inefficient and time-consuming.

## Objectives

- Automate plant care with minimal human effort.
- Provide real-time visual feedback through an LED display and emoji indicators.
- Prevent common issues such as overwatering and poor lighting.
- Build a cost-effective and scalable solution for different environments.

## Features

- Real-time monitoring: continuously reads soil moisture, light, temperature and humidity.
- Emoji feedback: a Pygame GUI shows happy or sad faces based on soil conditions (dry = sad, wet = happy).
- Audio alerts: plays sounds when the soil is too dry or too wet.
- Automatic LED control: an LDR senses ambient light and turns the LEDs on or off.
- Temperature and humidity logging: a DHT11 sensor records air conditions.
- User alerts: notifies the user when the plant needs attention.

## Components

### Hardware

| Component              | Role                                                              |
|------------------------|-------------------------------------------------------------------|
| Raspberry Pi 4         | Central processing unit                                           |
| Soil moisture sensor   | Measures soil water content                                       |
| ADS1115 (16-bit I2C)   | Converts the analog soil sensor output to digital for the Pi      |
| LDR                    | Detects ambient light intensity                                   |
| DHT11                  | Measures temperature and humidity                                 |
| LEDs                   | Visual indicators, controlled by light level and sensor thresholds|
| Capacitor (10 uF)      | Supports the LDR light-sensing circuit                            |
| Resistors              | Current limiting for LEDs and pull-down for the LDR               |
| Breadboard and jumpers | Prototyping and connections                                       |
| Monitor (HDMI)         | Displays readings and emoji interface                             |
| Speaker                | Audio alerts                                                      |

### Software

| Tool           | Role                                       |
|----------------|--------------------------------------------|
| Raspberry Pi OS| Operating system                           |
| Python         | Sensor reading and decision logic          |
| Thonny IDE     | Development environment                    |
| Pygame         | GUI with emoji visuals and sound           |

## Working

1. The soil moisture sensor outputs an analog signal, which the ADS1115 converts to digital and sends to the Raspberry Pi over I2C.
2. The LDR and DHT11 are read directly through GPIO pins.
3. The Raspberry Pi processes all readings in Python and compares them with preset thresholds.
4. Outputs are triggered:
   - The monitor shows readings and an emoji (happy or sad) for the plant status.
   - The speaker plays an alert when the soil is too dry or too wet.
   - The LEDs turn on in low light and may blink when humidity or soil moisture crosses a threshold.

## Applications

- Home gardening: indoor and outdoor plant care.
- Office and corporate spaces: plant care where natural light is limited.
- Greenhouses and agriculture: irrigation automation and placement optimisation.
- Smart homes and IoT: remote monitoring through mobile apps.
- Education and research: demonstrates IoT-based automation concepts.

## Future Scope

- AI-based plant health prediction and smart irrigation
- Mobile and cloud integration for remote monitoring and analytics
- Solar-powered operation
- Additional sensors for pH, nutrients and temperature
- Voice assistant integration (Alexa, Google Assistant)
- Scaling to greenhouses, smart cities and large-scale farming

