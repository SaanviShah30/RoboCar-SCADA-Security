#  RoboCar v1 – SCADA Security Project

**University at Albany | Jan 2025 – May 2025**

## What is this project?

I built a real remote-controlled vehicle using a Raspberry Pi computer and programmed it to work like an industrial SCADA control system. SCADA systems are used in factories, power plants, and water treatment facilities to control physical machines remotely. My vehicle simulated this environment so I could study and find the cybersecurity vulnerabilities that exist in these types of systems.

I built a Flask web application that acted as the control interface, similar to how SCADA operators control real machinery. I connected ultrasonic sensors for obstacle detection, motor drivers to control the wheels, and a live video stream for monitoring. I also installed Wazuh on the Raspberry Pi which is a security monitoring tool that detected unusual activity on the device.

## What vulnerabilities did I find?

The control webpage had no login or password protection, meaning anyone on the same network could take full control of the vehicle. All commands were sent without encryption which means an attacker could intercept and change the commands being sent. The Raspberry Pi still had its factory default password which is one of the most common security mistakes in IoT devices. The web interface also accepted any input without checking it first, which could allow command injection attacks.

## Project Photos

![RoboCar Front View](images/robocar_front.jpg)
![RoboCar Rear View](images/robocar_rear.jpg)

## Tools I used

Raspberry Pi · Raspbian OS · Python · Flask · Wazuh · GPIO · Motor Drivers · Sensors

## Skills this shows

ICS and SCADA security · IoT security · Embedded systems · Vulnerability assessment · Flask · Wazuh SIEM · Raspberry Pi hardware integration
