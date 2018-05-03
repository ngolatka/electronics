# led-nightlight

## Description
A simple, battery powered LED nightlight which automatically turns on when it's dark.

Power consumption is minimal. Batteries will typically last for several months. Using rechargeable NiMH batteries is recommended.

Quiescent current (LED off): typically around 40µA

Operating current (LED on): typically 3-5mA

## Operation
During daylight, the LDR's resistance is low, which turns on Q1. Q1 will then pull the base of Q2 to ground, which will therefore not conduct. The LED is off.

At night, the resistance of the LDR is high, therefore Q1 turns off. Current can now flow through R3 into the base of Q2, which will turn on, and the LED will light.

C1 is not strictly required, but creates a nicer "fading" effect when the LED turns on or off.
