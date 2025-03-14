** advance-home-automation-system**
ABSTRACTION :-
This project implements an MQTT-based IoT system that integrates ultrasonic distance measurement with relay control. The system consists of a rugged board equipped with an HC-SR04 ultrasonic sensor and a relay, controlled using the MRAA library.

The device connects to an MQTT broker and publishes telemetry data, including sensor readings.
It can be controlled remotely via MQTT messages, either manually (setValue command) or automatically (autoControl command).
The relay is triggered based on distance measurements, turning ON when an object is detected within a predefined range.
The system runs multiple threads for continuous telemetry publishing and autonomous relay control.
This implementation is ideal for smart automation applications like automatic door systems, obstacle detection, and remote-controlled relays.
PIN DIGRAM
1️⃣ Ultrasonic Sensor (HC-SR04) → IoT Board
HC-SR04    (A5D32X)Pin	Board Pin (GPIO)	    Description
VCC	            5V 	                   Power Supply
GND	            GND	                    Ground
TRIG	         GPIO 12	                Trigger Signal
ECHO	          GPIO 13	                 Echo Signal
2️⃣ Relay Module → IoT Board
Relay       (A5D2X) Pin	Board Pin (GPIO)	      Description
VCC	                5V	                  Power Supply
GND	                GND	                   Ground
IN	              GPIO 87 (PC23)	       Control Signal
