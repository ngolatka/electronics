# usb-nimh-charger

## Description
An extremely simple charging circuit for a single NiMH cell, powered by 5 V from a USB port or
power supply.

The circuit is designed to charge a flat 1900 mAh NiMH cell in 36 hours. Higher capacity cells
can be charged safely, but the charging time needs to be extended accordingly. A cell with a
lower capacity can also be charged, but care must be taken to not overcharge the cell, because
the charge current might not be in the safe region of 1/30 C (see notes below).

## Specifications
* Supply voltage: 5 V DC (stable)
* Minimal charging current: ~60 mA
* Maximum / short circuit current: ~90 mA
* Design cell capacity: 1900 mAh
* Charging time: 36 h for a completely flat 1900 mAh cell

## Components
* R1, R2, R3 120 Ω
* R4 390 Ω
* D1 1N4001
* LED (general purpose)
* Connector / holder for single cell

Resistors are rated 1/4 W. Tolerances are not critical.

## Notes
A typical NiMH cell can be safely
[trickle charged at around 1/30 C](https://en.wikipedia.org/wiki/Nickel%E2%80%93metal_hydride_battery#Trickle_charging),
therefore this circuit does not utilize any sophisticated way to detect the state of charge.
It will simply trickle charge the cell indefinitely.

The component values have been choosen to charge a NiMH cell with 60-90 mA. During charging,
the cell voltage will increase, which will reduce the current.

To charge more than one cell, the circuit must be built several times, one for each cell.
The diode D1 will prevent any current flow between the cells.

It is not advisable to simply use a single circuit and connect several cells in parallel

## Operation
The diode drops ~0,75 V, and the resistors drop between 2,75-3,4 V, depending on the
cell voltage. With a supply voltage of 5 V, this leaves a maximum charging voltage of 1,5 V.

At 1,5 V cell voltage, the charge current will be ~60 mA, which is in the safe region of 1/30 C
for a 1900 mAh cell. The charging process could continue indefinitely, but it is recommended
to terminate charging after 36-48 hours.

The LED will only light if current actually flows through the cell. A bad connection to the
cell can thus easily be identified. However, R4 and the LED are not strictly required for
operating the circuit.

The charging output is short-circuit proof by design, which protects the power source (e.g. a
computer's USB port) if a cell is defective.

## Acknowledgements
This circuit is partly based on the recommendation of [Big Clive](http://bigclive.com/) in
[this particular video]( https://www.youtube.com/watch?v=Lv23jMMPuiY).
