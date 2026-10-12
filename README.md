# Sensor and Actuator

# Automatic Night Light Using Arduino

## Description
This project uses an LDR sensor to detect light intensity
and automatically controls an LED.

## Components
- Arduino Uno
- LDR sensor
- 10k ohm resistor
- LED
- 220 ohm resistor
- Breadboard and jumper wires

## Working
The Arduino reads the LDR sensor every 500 milliseconds.
If the sensor reading is below 500, the LED turns ON.
Otherwise, the LED turns OFF.

## How to Run
1. Open the code in Arduino IDE or Wokwi.
2. Connect the components according to the wiring diagram.
3. Upload the code or start the simulation.
4. Observe the LED response to changes in light.

## Output
The LED automatically responds to the light level
detected by the LDR sensor.
