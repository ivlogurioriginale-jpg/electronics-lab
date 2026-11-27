# Arduino Traffic Light System 🚦

## Overview

This project demonstrates a simple traffic light system built using an Arduino UNO R3, three LEDs, and a breadboard.

The traffic light automatically switches between green, yellow, and red using predefined time intervals.

The project focuses on basic electronic circuits, digital output control, and timing using Arduino C++.

## Components Used

- 1 × Arduino UNO R3
- 1 × Breadboard
- 1 × Red LED
- 1 × Yellow LED
- 1 × Green LED
- 3 × Current-limiting resistors
- Jumper wires
- USB cable

## Circuit Connections

Each LED is connected to a separate Arduino digital output pin through its own current-limiting resistor.

| LED | Arduino Pin | Function |
|---|---|---|
| Red | D8 | Stop signal |
| Yellow | D9 | Warning signal |
| Green | D10 | Go signal |

All three LED circuits share a common ground (GND).

## How It Works

The Arduino controls the traffic light using three digital output pins.

The sequence is:

1. **Green LED ON** — 15 seconds
2. **Yellow LED ON** — 3 seconds
3. **Red LED ON** — 20 seconds
4. The sequence repeats continuously.

Only one LED is activated at a time.

The total duration of one complete cycle is **38 seconds**.

## Arduino Code

```cpp
void setup() {
  pinMode(8, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(10, OUTPUT);
}

void loop() {
  // Green light
  digitalWrite(8, LOW);
  digitalWrite(9, LOW);
  digitalWrite(10, HIGH);
  delay(15000);

  // Yellow light
  digitalWrite(8, LOW);
  digitalWrite(9, HIGH);
  digitalWrite(10, LOW);
  delay(3000);

  // Red light
  digitalWrite(8, HIGH);
  digitalWrite(9, LOW);
  digitalWrite(10, LOW);
  delay(20000);
}
```

## What I Learned

- How to build a circuit with three independently controlled LEDs
- How to connect multiple components to an Arduino UNO
- How to configure digital output pins using `pinMode()`
- How to control LEDs using `digitalWrite()`
- How to implement timing sequences using `delay()`
- How to create a continuously repeating control sequence using `loop()`
- How to test and troubleshoot a physical electronic circuit

## Project Photos

The project includes photographs showing the three traffic light states:

- Green LED activated
- Yellow LED activated
- Red LED activated

## Technologies Used

- Arduino UNO R3
- Arduino IDE
- C++
- Breadboard prototyping
- Basic digital electronics

## Future Improvements

Potential improvements include:

- Replacing `delay()` with `millis()` for non-blocking timing
- Adding a push button for manual control
- Adding an LCD to display the remaining time
- Implementing adjustable timing intervals

## Conclusion

This project demonstrates how a microcontroller can control multiple electronic components using a simple software-defined sequence.

It is part of my personal electronics learning journey, combining circuit construction with embedded programming.
