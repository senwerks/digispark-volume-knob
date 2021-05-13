# Digispark Volume Knob

Physical rotary volume knob using a Digispark and rotary encoder, via USB HID standard media controls.

Plugs into any PC/laptop or any other USB device that accepts standard media controls (like the media keys on your generic keyboards), and translates the rotary knob into volume up/down, and clicking the knob as mute/unmute.

## Ingredients

- [Digispark](http://digistump.com/products/1) (or any similar Attiny85 board)
- [Rotary Encoder](https://core-electronics.com.au/rotary-encoder-extras.html)
- 3D printer, wire, soldering gear, a table, probably a few snacks, etc.

## Instructions

Print the 3 STLs in the repository: [Chassis v1.stl](https://github.com/senwerks/digispark-volume-knob/blob/master/Chassis%20v1.stl), [Knob v1.stl](https://github.com/senwerks/digispark-volume-knob/blob/main/Knob%20v1.stl) (unless you're using the knob that came with the encoder, but I preferred my minimal design) and [Lid v1.stl](https://github.com/senwerks/digispark-volume-knob/blob/master/Lid%20v1.stl).

Mock the parts up inside the chassis to get an idea for wire lengths, then solder it all together outside of the chassis for better access. Check the encoder's [Data Sheet](https://cdn-shop.adafruit.com/datasheets/pec11.pdf) for pinouts if you're not sure, but the general idea is:

- Encoder channel A to Digispark pin 0
- Encoder channel B to Digispark pin 2
- Encoder common to Digispark pin GND
- Encoder switch pin 1 to Digispark pin 1
- Encoder switch pin 2 to Digispark 5V

![Digispark Volume Knob wiring](https://raw.githubusercontent.com/senwerks/digispark-volume-knob/main/Meta/DigisparkVolumeKnob-Wiring.jpg)

The code to load onto the Digispark is just the Adafruit ["Trinket USB Volume Knob" code](https://learn.adafruit.com/trinket-usb-volume-knob/add-a-mute-button), as their Trinket uses the same Attiny85 chip as the Digispark so they're 100% compatible. If you know what you're doing, you can copy/paste the code from my repository (don't forget to add the "TrinketHidCombo.h" library before compiling) or if you need more details, follow [their tutorial here](https://learn.adafruit.com/trinket-usb-volume-knob/code) and make sure you use the extra code from the "Add a Mute Button" page if you got an encoder with clicky switch.

I then used a bit of 3M double-sided tape to stick the encoder to the chassis piece and keep it stable (yet still be able to peel it off if it fails and needs to be replaced), or you could use hot glue, and then crammed all the wiring in:



![Digispark Volume Knob parts](https://raw.githubusercontent.com/senwerks/digispark-volume-knob/main/Meta/DigisparkVolumeKnob-Parts.jpg)

![Digispark Volume Knob assembly](https://raw.githubusercontent.com/senwerks/digispark-volume-knob/main/Meta/DigisparkVolumeKnob-Assembly.jpg)

The lid clicks onto the chassis (and is easily removable for repairs later), and then the knob clips onto the top of the encoder. NOTE: You might need to print the knob at 102% size if it's a bit too tight on your encoder, depends on your printers tolerances.

Depending on your laptop/device you can plug it directly into the USB port, or I use a small USB extension cable from my PC to have the knob sitting directly to the right of my mouse for easy volume adjustments.

![Digispark Volume Knob on a laptop](https://raw.githubusercontent.com/senwerks/digispark-volume-knob/main/Meta/DigisparkVolumeKnob-Laptop.jpg)

![Digispark Volume Knob on a PC](https://raw.githubusercontent.com/senwerks/digispark-volume-knob/main/Meta/DigisparkVolumeKnob-Desktop.jpg)

Contact me via [@senwerks](https://twitter.com/senwerks) if you need any help or have any feedback/improvements!