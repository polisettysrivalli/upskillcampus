# Smart Home Automation using Embedded Systems and IoT

## Project Overview

This project implements a Smart Home Automation system using embedded systems and Internet of Things (IoT) technologies. The system allows users to control home appliances such as lights and fans remotely using a mobile application through Bluetooth or WiFi communication.

The project is developed as part of the Industrial Internship program conducted by upskill Campus in collaboration with UniConverge Technologies Pvt Ltd.

---

## Objective

The objective of this project is to design and implement a system that enables remote monitoring and control of household appliances using a microcontroller and communication module.

---

## Components Used

* Arduino Uno
* HC-05 Bluetooth Module / WiFi Module
* Relay Module
* Light / Fan (Home Appliances)
* Jumper Wires
* Power Supply

---

## Block Diagram

Mobile Application → Communication Module → Arduino Microcontroller → Relay Module → Home Appliances

---

## System Working

1. The user sends a command from the mobile application.
2. The Bluetooth/WiFi module receives the command.
3. The Arduino microcontroller processes the received command.
4. The relay module switches the connected appliance ON or OFF.
5. The appliance operates according to the received command.

---

## Arduino Code

```cpp
char data;
int light = 7;
int fan = 8;

void setup() {
  Serial.begin(9600);
  pinMode(light, OUTPUT);
  pinMode(fan, OUTPUT);
}

void loop() {
  if (Serial.available() > 0) {
    data = Serial.read();
  }

  if (data == 'A') {
    digitalWrite(light, HIGH);
  }

  if (data == 'a') {
    digitalWrite(light, LOW);
  }

  if (data == 'B') {
    digitalWrite(fan, HIGH);
  }

  if (data == 'b') {
    digitalWrite(fan, LOW);
  }
}
```

---

## Results

The Smart Home Automation system successfully controls home appliances remotely. The system demonstrates how embedded systems and IoT technologies can be used to improve convenience, automation, and energy efficiency in modern homes.

---

## Internship Details

Industrial Internship Program
Organized by upskill Campus
In collaboration with UniConverge Technologies Pvt Ltd

Student Name: Polisetty Srivalli
Branch: Electronics and Communication Engineering (ECE)
College: Vignan's Lara Institute of Technology and Science
