# EchoEye
EchoEye – Rotational detection system
This project implements a real-time sonar scanning system using an HC-SR04 ultrasonic sensor mounted on a servo motor. EchoEye rotates the sensor in a 180° arc, allowing continuous scanning of a semicircular space. The measured distances are transmitted via the serial port to a visualization program that graphically displays, in radar style, all objects detected in the field of action.
EchoEye operates on two distinct software components: the firmware loaded on the Arduino board manages the motor movement and sensor readings, while the visualization application (made in Processing IDE) interprets the received data and displays it in the form of an animated radar, with green lines for free space and red lines for objects detected within the configured range.
Hardware connections:
Senzor ultrasonic HC-SR04:

VCC → 5V
GND → GND
TRIG → Pin digital 2
ECHO → Pin digital 3

Servomotor:

Red → 5V
Brown → GND
Orange → Digital pin 4

Operating mode:
When turned on, EchoEye starts rotating the sensor from 0° to 180° and back, in a continuous loop. At each degree of rotation, the sensor emits an ultrasonic pulse and measures the return time of the echo, calculating the distance to any obstacles. If an object is within the configured detection range (default 40 cm), it appears highlighted on the radar display. The data is transmitted serially and interpreted visually in real time.
