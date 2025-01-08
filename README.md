Name:PALURI SRAVANI  Company: CodTech IT Solutions Pvt. Ltd Intern ID: CT12EFN Domain: Embedded Systems Duration: December 17, 2024, to February 17, 2025

Project Overview Project Title: Use a Temperature Sensor to Read and Display Temperature Data on an LCD or Serial Monitor

Objective To build a system that reads temperature data using a sensor and displays it on an LCD screen or the Arduino Serial Monitor for real-time monitoring.

Components Required Arduino Uno/Nano: Microcontroller to process data. Temperature Sensor: LM35, DHT11, or DHT22 to measure temperature. 16x2 LCD: Display temperature readings (with or without I2C module). Breadboard and Jumper Wires: For circuit connections.

Connections

For LM35 Sensor VCC → 5V (Arduino) GND → GND (Arduino) OUT → A0 (Arduino)
For DHT11/DHT22 Sensor VCC → 5V (Arduino) GND → GND (Arduino) DATA → Digital pin (e.g., D2)
For LCD (With I2C Module) SDA → A4 (Arduino Uno) SCL → A5 (Arduino Uno) VCC → 5V GND → GND
How It Works

Temperature Sensor Working Principle LM35:
Converts temperature into voltage (10mV per °C). For example: At 25°C, the output voltage is 250mV (0.25V). DHT11/DHT22:

Measures temperature digitally. Sends the data using digital communication. Requires the DHT library to decode data. 2. Arduino Processing For LM35:

The Arduino reads the analog voltage using the analogRead() function. Converts the voltage into a temperature value using the formula: Temperature (°C)
Voltage (mV) / 10 Temperature (°C)=Voltage (mV)/10 Displays the result on the LCD or Serial Monitor. For DHT11/DHT22:

The library handles the decoding of digital data. The Arduino uses the readTemperature() function to fetch the temperature. 3. Display Output LCD: The temperature value is formatted and shown on a 16x2 LCD screen. Serial Monitor: Data is sent via USB to the Serial Monitor, providing an alternative display for debugging or monitoring when the LCD is not used.

![WhatsApp Image 2025-01-08 at 11 02 29 AM](https://github.com/user-attachments/assets/d1925348-34cf-461b-91c1-28f292528a1b)
