# usb-nimh-charger

## Description
An extremely simple charging circuit for NiMH cells, powered by 5V from a USB port.

A typical AA cell with 1900mAH will take roughly 36 hours to charge (if completely flat).

Because NiMH cells can be trickle charged at around 1/3 C indefinitely, this circuit does not need any sophisticated way to detect the state of charge. It will simply trickle charge the cell continuously.

## Operation
All component values have been choosen to charge a NiMH cell with 60-90mA.

Depending on the cell voltage, the current will vary. The higher the cell voltage, the lower the current. At 1,5V cell voltage, the charge current will be roughly 60mA, which is in the safe region of 1/3 C for a typical 1900mAh cell.

The resistors R1, R2, and R3 are rated for 1/4 watt. To spread the dissipation, several resistors are used instead of a single one.

## Acknowledgements
This circuit is partly based on the recommendation of Big Clive https://www.youtube.com/user/bigclivedotcom in this particular video https://www.youtube.com/watch?v=Lv23jMMPuiY
