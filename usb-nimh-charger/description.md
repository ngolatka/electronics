# usb-nimh-charger

## Description
An extremely simple charging circuit for NiMH cells, powered by 5V from a USB port.

A typical AA cell with 1900mAh will take roughly 36 hours to charge (if completely flat).

Because NiMH cells can be trickle charged at around 1/3 C indefinitely, this circuit does
not come with any sophisticated way to detect the state of charge. It will simply trickle
charge the cell continuously.

## Operation
The component values have been choosen to charge a NiMH cell with 60-90mA.

The diode will drop 0,75V, and the resistors drop between 2,75 - 3,4V, depending on the
cell voltage.

The higher the cell voltage, the lower the current. At 1,5V cell voltage, the charge current
will be roughly 60mA, which is in the safe region of 1/3 C for a typical 1900mAh cell.

The resistors R1, R2, and R3 are rated at 1/4 watt. To spread the dissipation, several
resistors are used in parallel instead of a single one.

The LED will only light if current actually flows through the cell. A bad connection to the
cell can thus easily be identified. However, R4 and the LED are not strictly required for
operating the circuit.

The charging output is short-circuit proof by design, which protects the power source (e.g. a
computer's USB port). The maximum current is ~100mA.

## Acknowledgements
This circuit is partly based on the recommendation of [Big Clive](http://bigclive.com/) in
[this particular video]( https://www.youtube.com/watch?v=Lv23jMMPuiY).
