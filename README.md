# IOT_PROJECT
IoT technologies to create a safer and more responsive mining environment, fostering increased efficiency and reducing the likelihood of accidents or health hazards for workers in the coal mining industry using Arduino Uno, ESP8266, and multiple sensors.
This code is designed for an IoT (Internet of Things) project that involves monitoring temperature, humidity, light, gas, and rain conditions using various sensors. Let's break down the code and explain the purpose of each section.
![20231204_001553](https://github.com/user-attachments/assets/d6348f33-bf6e-40fb-81e1-d700736accb1)
Libraries and Definitions:

The code includes necessary libraries like Blynk, ESP8266WiFi, and DHT for working with the Blynk app, connecting to Wi-Fi, and handling the DHT11 sensor, respectively.
It defines the Blynk template ID, name, and authentication token for connecting to the Blynk server.
It sets up pins for a buzzer, a rain sensor, an LDR (Light Dependent Resistor), and an MQ2 gas sensor.
Setup Function:

Initializes serial communication for debugging purposes.
Begins the Blynk connection with the provided authentication token, Wi-Fi SSID, and password.
Initializes the DHT sensor, LDR, and sets up the pin modes for the buzzer.
Commented sections indicate that there were attempts to set up a rain sensor, but it's currently disabled.
Loop Function:

Runs the Blynk service.
Reads temperature and humidity values from the DHT sensor.
Checks if the readings are valid and sends them to the Blynk app.
Monitors the LDR, turning on an LED if it detects light.
Reads the analog value from the MQ2 gas sensor and activates a buzzer if the value is above a certain threshold.
Currently, the rain sensor functionality is commented out.
Blynk Integration:

Sends temperature, humidity, LDR state, and gas sensor values to the Blynk app using virtual pins (V0, V1, V2, V5).
Additional Comments:

There are commented-out sections related to a rain sensor. If enabled, it could detect rain conditions and provide feedback.
The code attempts to handle rain conditions by setting a rainBool variable. However, this part is incomplete and needs further development.
There's a delay of 2 seconds after each sensor reading and Blynk update.
Overall Importance:
This code demonstrates the integration of various sensors to monitor environmental conditions. The project aims to provide real-time data on temperature, humidity, light, and gas levels, making it suitable for applications such as home automation, weather monitoring, or environmental sensing. The Blynk integration allows users to remotely monitor these conditions through a mobile app. The code serves as a foundation for a comprehensive IoT system that can be expanded with additional sensors and functionalities.
