![afterglow](https://github.com/smyp/afterglow/blob/master/artwork/afterglow.png "Afterglow")

AFTERGLOW is a pinball machine extension board that aims at softening the hard lamp on/off transitions which are the consequence of replacing the original incandescent bulbs with LEDs. It works with Williams WPC, Williams System 11, Data East and probably also with Sega games.

The brain of the board is a Arduino nano. It samples the original lamp matrix from the WPC Power Driver Board using two parallel to serial shift registers.

The basic principle involves resampling of the original lamp matrix signals at 4kHz. This allows for PWM LED dimming with 3 bits (8 brightness steps).

The resampled signal is output via serial to parallel shift registers driving 16 MOSFETs.

Make sure to check the ![wiki](https://github.com/smyp/afterglow/wiki) for detailed information and instructions.

### Quick guide to the board revisions

#### WPC, WPC-95, System 11, Data East, Sega
* *PCB v1.3*<br/>This is the *preferred board revision* for these games.<br/>Dedicated power input (+18V, Ground) must be connected separately to power driver board
* *PCB v1.4*<br/>Except for power input exactly the same as revision 1.3<br/>+18V taken from column input.<br/>⚠ Ground must still be connected to the PDB! Failure to do so will damage the board!
* *PCB v1.5*<br/>Same as v1.4, but using a one-sided PCB. This should be easier/cheaper for automated production than v1.4.

#### Stern Whitestar (and possibly S.A.M.)
* *PCB v2.1* Dedicated board which will only work with Stern Whitestar and possibly S.A.M. games

### Pictures

#### PCB v1.3
![afterglow](https://github.com/smyp/afterglow/blob/master/docu/images/pcb_v13_populated.jpg "Afterglow PCB v1.3")


