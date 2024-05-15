# Human-Following-Robot

There are several technologies that can detect and maintain a certain distance between a Robot and a Human. The most commonly used are ultrasonic sensors, infrared sensors, laser range sensor, voice and face recognition camera sensors etc..

I introduce you to the Arduino Robot, which uses a combination of Ultrasonic and infrared sensors to track an object. The device is really very simple to build and very effective, so it has been presented several times on the Internet. Most often in these presentations a servo motor is used which moves the ultrasonic sensor. This servo motor has no role in the operation of the Robot, except the visual one at the beginning, and complicates it unnecessarily. In my project I removed this servo, in order to simplify.

The robot consists of several components:

- Arduino Uno microcontroller

- L293D Motor driver shield

- 4pcs. DC gear motors with Weels

- HC-SR04 Ultrasonic sensor module

- 2 Infrared sensor boards

- and 7.4 Volts Lithium-Ion Battery pack

To make it, we need only one rectangular plate, on which lower side should be glued the engines, and on the upper surface are mounted other elements. You can use discontinued L293D motor driver shield like in my case, but also and Adafruit motor shield as is presented on the schematic diagram without any changes.


The principle of object detection and monitoring is based on data accepted by both sensors. The ultrasonic sensor detects the presence of an object in front of it within certain limits, in our case between 10 and 30 centimeters. If there is no object (for example our hand) in this space, all four engines are idle. At the moment when an object appears in this space, the data from the infrared sensors are read, and based on the obtained data, commands are given to the motors, whereby the robot moves in the desired direction. The distance to which the infrared sensors respond is adjusted by a small triming potentiometer. This distance should be adjusted so that it is slightly larger than the minimum distance to which the ultrasonic sensor is set to respond, in our case it is more than 10 centimeters.

