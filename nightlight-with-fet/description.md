# nightlight-with-fet

## Description
A simple, battery powered LED nightlight which automatically turns on when it's dark.

Power consumption is minimal. Batteries will typically last for several months.

Recommended operating voltage: 3,5 - 4,5V (e.g. three AA cells).

Quiescent current (LED off): typically less than 5µA

Operating current (LED on): typically 5-10mA

## Note
If two NiMH cells are used (giving nominally only 2,4V), R1 should be decreased to 100k.
Otherwise the gate voltage of Q1 might not rise high enough to turn Q1 on. The lower R1
will increase the quiescent current slightly to around 30µA. Using three AA cells is
therefore recommended, because this also allows driving white LEDs at nominal power.

## Operation
During daylight, the LDR's resistance is low, which pulls the gate voltage of Q1 low. Q1
will not conduct. The LED is off.

At night, the resistance of the LDR is high, which allows the gate voltage to rise until
Q1 turns on, and the LED will light.
