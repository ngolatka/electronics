# led-nightlight

## Description
A simple, battery powered LED nightlight which automatically turns on when it's dark.

Power consumption is minimal. Batteries will typically last for several months. Using
rechargeable NiMH cells is recommended.

## Specifications
* Supply voltage: 2,4 - 3V (two AA alkaline or NiMH cells)
* Quiescent current: typically 40µA
* Operating current: 3-5mA

## Components
* R1 220k
* R2, R3 100k
* R4 220R
* LDR (general purpose)
* Q1, Q2 BC547
* C1 47µF, 10V
* LED 5mm 16000mcd
* 2 AA cells (alkaline or NiMH)

Resistors are rated 1/4W. Tolerances are not critical.

If white LED is used, 3 AA cells are recommended.

## Operation
During daylight, the LDR's resistance is low, which turns on Q1. Q1 will then pull the
base of Q2 to ground, which will therefore not conduct. The LED is off.

At night, the resistance of the LDR is high, therefore Q1 turns off. Current can now flow
through R3 into the base of Q2, which will turn on, and the LED will light.

C1 is not strictly required, but creates a nicer "fading" effect when the LED turns on or
off.
