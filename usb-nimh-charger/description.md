# usb-nimh-charger

## Description
An extremely simple charging circuit for a NiMH cell, powered by 5V from a USB port.

Because NiMH cells can be trickle charged at around 1/3 C indefinitely, this circuit does
not utilize any sophisticated way to detect the state of charge. It will simply trickle
charge the cell continuously.

## Specifications
* Supply voltage: 5V (from USB port)
* Minimal charging current: 60mA
* Maximum / short circuit current: 90mA
* Expected cell capacity: 1900mAh
* Charging time: 36h for a completely flat cell

## Components
* R1, R2, R3 120R
* R4 390R
* D1 1N4001
* LED (general purpose indicator)
* Connector / holder for cell

Resistors are rated 1/4W. Tolerances are not critical.

## Operation
The component values have been choosen to charge a NiMH cell with 60-90mA. During charging,
the cell voltage will increase, which will reduce the current.

The diode will drop 0,75V, and the resistors drop between 2,75 - 3,4V, depending on the
cell voltage. With a supply voltage of 5V, this leaves a maximum charging voltage of 1,5V.

At 1,5V cell voltage, the charge current will be ~60mA, which is in the safe region of 1/3 C
for a 1900mAh cell.

The resistors R1, R2, and R3 are rated at 1/4 watt. To spread the dissipation, several
resistors are used in parallel instead of a single one.

The LED will only light if current actually flows through the cell. A bad connection to the
cell can thus easily be identified. However, R4 and the LED are not strictly required for
operating the circuit.

The charging output is short-circuit proof by design, which protects the power source (e.g. a
computer's USB port).

## Acknowledgements
This circuit is partly based on the recommendation of [Big Clive](http://bigclive.com/) in
[this particular video]( https://www.youtube.com/watch?v=Lv23jMMPuiY).
