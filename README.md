A small PCB that uses a  OPA1679 op amp to amplify a signal from piezolectric crystals.



It has balanced output,input and should run on +48 phantom power.
Shielded cable must be used for connection to the piezo crystals.
Please use 0,5 W metal film resistors with 1% tolerance or better and audio quality capacitors.
Polypropylene (PP) capacitators is good, electrolytes if needed.

It is important that the circuit board is mounted inside a metal box, and Ø2mm conducting metal standoffs are used.
The corner pads of the PCB board is reserved for that.
Of course the PCB board and components must not come in contact with any metal surface expect the standoffs.

The circuit may benefit from a Zobel network, that is a 680 pF capacitor and a 150 ohms resistor in series between pin 2 and 3 on the output or the input connector. It should avoid high frequency oscillation in a long cable.

Schematic diagram: 
https://raw.githubusercontent.com/Supermagnum/HighZ-stereo/refs/heads/main/Highz-stereo.pdf

Component side:

https://github.com/Supermagnum/HighZ-stereo/blob/main/components-side.jpg

Reverse side:
https://github.com/Supermagnum/HighZ-stereo/blob/main/back-side.jpg

PCB board dimensions: 62.5X97.5 mm

BOM files:
https://github.com/Supermagnum/HighZ-stereo/tree/main/BOM-files
note: two ZPD11 zener diodes is missing from the BOM.

Piezoelectric disk, red wire for positive polarity.
Black for negative: https://github.com/Supermagnum/double-gain/blob/main/Piezo-element-6.jpg

They usually have a 3 pin XLR plug. Those are wired up like this: https://github.com/Supermagnum/piezo-balanced/blob/main/XLR%2BConnector%2BPinout%2BDiagram%2BRear%2BPin%2B2%2BHot%2Bv2%2Bgreen__01.jpg

NOTE:  
The XLR 3 pin plug has a solder lug for the shield for a reason.
It is my opinion that a shielded cable with 3 conductors inside is the best.
Suggested cable: Digi-Key Part Number:3242SL005-ND

Based on:
http://www.richardmudhar.com/blog/piezo-contact-microphone-hi-z-amplifier-low-noise-version/

Why: The problem with piezo guitar pickups and piezoelectric crystals is that they are not well matched to typical audio inputs. By their nature they can generate a lot of signal, but they cannot drive a 50 kilohm typical line input. The pickup needs to work into a much higher impedance, typically 1 megohm or so.

So what to people do? They go and plug a piezoelectric disks output directly into the line input of their recorder, typical impedance 50k, or the plug-in-power mic input of their recorder, typical impedance about 7k, and they start to bitch and moan that this damn thing sounds tinny. Which is does ! But they don't understand why!

The reason why these devices often sound tinny is because the piezo sensor presents its signal through a series capacitance which is small, typically 15nF or less. When wired to a normal 50 kilohm line input this forms a high-pass filter, which eliminates the bass.

This circuit board solves that, and amplifies the signal. How many dB it amplifies is dependent on the resistance on the resistors used.The data for that is on the schematic diagram.

It's fairly easy and straight forward to solder the components to the circuit board, a nice pointy soldering iron, solder, a magnifying glass, and a ohm or multimeter is all that is needed. Of course one needs a suitable metal box, and the circuit boards components must not come in contact with the metal box. That will cause short circuit, so it's best mounted on stand offs. Also, use the magnifying glass to check that no one of the soldering pads has been bridged.

It can be used for two reverb plates, listening to the insides of a engine,recording the sound of vibrating things. You will need 4 piezoelectric disks for that, mounted in two metal boxes Non electric conductive super glue is useable for that. Just glue them to a flat surface. The piezoelectric disks should be electrically insulated from the metal box.

Of course one can use a recorder like a tascam dr40x, as long as it can supply +48 volt phantom power, and has a headphone jack for monitoring.

A good set of headphones or ear protection with built in speakers will keep out unwanted sounds or noise.

Should also work nice with hydrophones. PZT-5H tubes is best for that. You want more gain, 35 or 40 dB for that. 
In case of dual hydrophones it's possible to have the hydrophones attached with two long cables. 

Some interesting ideas can be found in: https://github.com/Supermagnum/piezo-balanced/blob/main/Barlow-et-al-2008-HydrophoneConstruction_TM-417.pdf Note: Ecopoxy Flowcast does not need any vacuum, just a mold and a way to hold the piezoelectric tubes centered. It's also safer to work with.

Some methods of mounting a piezoelectric disk can be found here: https://locusonus.org/wiki/index.php?page=Hydrophone.en

Made with: http://www.kicad.org/

KiCad uses an integrated environment for all of the stages of the design process: Schematic capture, PCB layout, Gerber file generation/visualization, and library editing.

KiCad is a cross-platform program, and free!



