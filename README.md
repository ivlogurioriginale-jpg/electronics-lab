# Arduino Dual LED Control

## Overview
A beginner electronics project using an Arduino UNO R3 to control two LEDs independently through digital output pins.

The LEDs turn on alternately at one-second intervals, demonstrating basic digital output control, circuit connections, and Arduino programming.

## Components
- Arduino UNO R3
- Breadboard
- 2 LEDs
- 2 current-limiting resistors
- Jumper wires
- USB cable

## Circuit Connections

**LED 1**
- Arduino D8 → Breadboard A2
- Resistor: B2 → C7
- LED anode (+): D7
- LED cathode (-): D12
- Arduino GND → A12

**LED 2**
- Arduino D9 → Breadboard B22
- Resistor: C22 → D28
- LED anode (+): E28
- LED cathode (-): E32
- Common ground: B12 → A32

## How It Works

The Arduino controls both LEDs using digital output pins 8 and 9.

1. LED 1 turns ON while LED 2 remains OFF.
2. After one second, LED 1 turns OFF and LED 2 turns ON.
3. After another second, the sequence repeats continuously.

The program uses `pinMode()`, `digitalWrite()`, and `delay()`.

## What I Learned

- How breadboard connections work
- How to build independent LED branches
- How to control digital outputs using Arduino C++
- How to use resistors to limit LED current
- Basic hardware and software troubleshooting

## Hardware

A photograph of the completed breadboard circuit is included in the project files.

## Technologies

Arduino UNO R3 · C++ · Arduino IDE · Breadboard
