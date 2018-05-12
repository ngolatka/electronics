# led-nightlight

## Description
A simple, battery powered LED nightlight which automatically turns on when it's dark.

Power consumption is minimal. Batteries will typically last for several months. Using
rechargeable NiMH cells is recommended.

## Specifications
* Supply voltage: 2,4-3 V (two AA alkaline or NiMH cells)
* Quiescent current: typically 40 µA
* Operating current: 3-5 mA

## Components
* R1 220 kΩ
* R2, R3 100 kΩ
* R4 220 Ω
* LDR (general purpose)
* Q1, Q2 BC547
* C1 47 µF, 10 V
* LED 5 mm 16000 mcd
* 2 AA cells (alkaline or NiMH)

Resistors are rated 1/4 W. Tolerances are not critical.

If white LED is used, 3 AA cells are recommended.

## Operation
During daylight, the LDR's resistance is low, which turns on Q1. Q1 will then pull the
base of Q2 to ground, which will therefore not conduct. The LED is off.

At night, the resistance of the LDR is high, therefore Q1 turns off. Current can now flow
through R3 into the base of Q2, which will turn on, and the LED will light.

C1 is not strictly required, but creates a nice "fading" effect when the LED turns on or
off.
