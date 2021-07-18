## Squascillator: Square-wave AVR VCO

A square-wave oscillator with voltage-controlled duty cycle - this one is built around a microcontroller, rather than an analogue, core so far fewer components are required to get things up and running and it's far less hassle to calibrate; there's a fine-tune trimmer on the board but most of the heavy-lifting is done by the firmware.

Note the two CV inputs - one has an attenuator (CV1) whilst the other hasn't.  Inputs from the two are mixed, and the CV2 input is pulled to ground by default.

Like my other AVR-based VCOs, this one will track 1V/oct pretty well over 5 octaves, although if you're expecting 'to-the-cent' accuracy then you may well be disappointed unless you're prepared to hack on the firmware (specifically, fine-tune the values in the pitch lookup table - have fun!)

Square waves aren't as boring as they seem - with a bit of judicious filtering (resonant or otherwise) you can get some pretty crazy sounds from your bog-standard square, and team a couple of these up with something like the CLOCK-LOGIC module and you've got a recipe for wild and crazy sounds.

### Build notes

There are no special build requirements - the parts count is actually quite low. There are a pair of surface-mount Schmitt trigger inverters but these are pre-soldered.

Both pots should be linear taper - pretty much any value will work fine (I recommend 10k or 20k). 50k is a good value for the fine-tune trimmer.

The Squascillator and the XO106r5 share the same firmware.
