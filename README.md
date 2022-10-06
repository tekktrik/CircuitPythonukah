# CircuitPythonukiah Hardware
Hardware required for the CircuitPythonukiah project

## Hardware Dependencies
Here are all the things needed: to physically build your very own CircuitPythonukiah:

### Custom Components

The project makes use of two custom parts. The first is the custom PCB that is the heart
of the CircuitPythonukiah.  The second is a base that can be 3D printed, which holds the
PCB upright.  You can find the PCB KiCAD design and fabrication files in the
`electrical/` folder, and you can find both the PCB's STEP file representation, as well
as the STEP and STL files for the base in the `mechanical/` folder.

### Mechanical (Off-The-Shelf)

This project uses the following off-the-shelf mechanical components:

* [Self-Tapping M5 Screw](https://www.mcmaster.com/90380A392/) (x1)
* [M5 Spacer](https://www.mcmaster.com/7298N112/) (x1)

### Electronics (Off-The-Shelf)
This project uses the following off-the-shelf electronic components:

* [QT Py ESP32-S2 Dev Board](https://www.adafruit.com/product/5325) (x1)
* [Piezo Buzzer](https://www.adafruit.com/product/160) (x1)
* [Slide Switch](https://www.digikey.com/en/products/detail/e-switch/EG1218/101726)
* [Super Bright Yellow 5mm LED](https://www.adafruit.com/product/2700>) (x9)
* [100 Ohm Resistor](https://www.digikey.com/en/products/detail/yageo/CFR-25JB-52-100R/246) (x9)
* [Male Header Pins (7 position)](https://www.digikey.com/en/products/detail/harwin-inc/M20-9770746/3727778) (x2)
* [Female Header Pins (7 position)](https://www.digikey.com/en/products/detail/sullins-connector-solutions/PPPC071LFBN-RC/810179) (x2)
* [USB C Receptacle](https://www.digikey.com/en/products/detail/cui-devices/UJC-VP-3-SMT-TR/14310511) (x1)


## Building Hardware

### Fabricating the Custom Components

There isn't necessarily one way to do this, but I can mention how I did it:

I used [JLCPCB](https://jlcpcb.com/) to fabricate my boards, mostly because I knew
they could do blue PCBs and the quote for the weirdly shaped PCB was better than
others I had looked at.

For the base, I used 0.2 mm layer thickness and 20% infill.  I also didn't use supports
when I printed since it came out pretty well without them, and I had a lot of trouble
removing the breakway supports otherwise.  I'm leaving it up to [Hubs](https://www.hubs.com/)
(the printing service I'll be using) to figure that last bit out (not sure I can specify
either).  I decided to print this in black rather than blue since the black made the
board "pop" more.

### Soldering the PCB

This is by far the most labor-intensive step.  Since I didn't plan on this being any
kind of big operation, I decided to hand-solder eerything to the board.  This was fairly
straight forward with the exception of a couple things:

* I would bend each LED so the pins so would be in just about the right place, and then I
  bend the wires again to somewhat lock it in place.  I'd then solder one pin to the board,
  while using one hand to hold the LED and PCB, and the other to use the soldering iron,
  which would allow me to remelt the solder and use my hand to finely position the LED.
* The USB C receptacle was a byproduct of not wanting multiple USB receptacle types
  between the microcontroller and the PCB.  I found that I could do a similar trick as
  the LED and solder one pad to "lock" it, and then use one hand to apply pressure while
  remelting the solder with the other.  Then I just applied solder across the pads, using
  some solder wick to get all the extra.

### Assembling Everything

I used a small hand tool to screw in the self-tapping screw, which helped make sure the board
wasn't rattling too much when everything is assembled.  Don't forget to add the spacer before
tightening everything!
