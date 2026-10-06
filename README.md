# Sensor and Actuator

## Project Overview

This project demonstrates a simple embedded system that reads a sensor value and controls an output based on the reading.

An **LDR (Light Dependent Resistor)** is used as the sensor to detect the surrounding light level. An **LED** is used as the actuator/output. The Arduino reads the LDR value every 500 milliseconds and controls the LED according to the detected light level.

## Objective

The main objective of this project is to demonstrate:

* Reading data from a sensor
* Processing the sensor reading using Arduino
* Controlling an output based on the sensor value
* Reading the sensor at a fixed interval
* Implementing a simple sensor-to-actuator system

## Components Used

* Arduino Uno
* LDR (Light Dependent Resistor)
* 10kΩ Resistor
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires

## Sensor

**LDR (Light Dependent Resistor)**

The LDR detects the amount of light in the surrounding environment. Its resistance changes depending on the intensity of light.

The LDR is connected to analog pin **A0** of the Arduino.

## Actuator / Output

**LED**

The LED acts as the output device. It responds to the LDR sensor reading.

* Dark environment → LED ON
* Bright environment → LED OFF

## Wiring Diagram

The complete circuit connection is shown below.

![Wiring Diagram](wiring-diagram.png)

## Connections

### LDR

```text
5V
 |
LDR
 |
 +-------- A0
 |
10kΩ
 |
GND
```

### LED

```text
Arduino D13
     |
   220Ω
     |
    LED
     |
    GND
```

## Working

1. The Arduino reads the LDR sensor through analog pin A0.
2. The sensor is read every **500 milliseconds**.
3. The Arduino compares the sensor value with a predefined threshold.
4. If the environment is dark, the LED turns ON.
5. If the environment is bright, the LED turns OFF.
6. The sensor value is displayed in the Serial Monitor.

## Sensor Reading Interval

The sensor is read once every **500 milliseconds**.

This interval provides a simple and responsive way to detect changes in light intensity.

## Expected Output

| Environment | LED |
| ----------- | --- |
| Dark        | ON  |
| Bright      | OFF |

## How to Run

1. Install the Arduino IDE.
2. Open `automatic_light.ino`.
3. Connect the Arduino and components according to the wiring diagram.
4. Connect the Arduino Uno to the computer.
5. Select the Arduino Uno board and correct COM port.
6. Upload the program.
7. Open the Serial Monitor at **9600 baud**.
8. Change the amount of light falling on the LDR.
9. Observe the LED response.

## Repository Structure

```text
sensor-and-actuator/
│
├── automatic_light.ino
├── wiring-diagram.png
└── README.md
```

## Conclusion

This project demonstrates a basic embedded system in which an LDR sensor provides input to an Arduino and an LED responds to the sensor reading. It shows the fundamental relationship between a **sensor, microcontroller, and actuator**.
