# RGB Video Modification
## Background
This design is based on the Matra Alice schematic.  The Alice outputs an RGB+Audio signal via a 7-pin DIN socket - this would normally be connected to a Peritel or SCART connector.<br>

## Design Notes
### Transistor Replacements
The original design uses obsolete transistors: BC172c (NPN) and BC252c (PNP).  I've tried to match with available transistors - not an expert, happy to be advised of better matches:<br>
BC172c -> 2N3904<br>
BC252c -> BC558<br>

### Video Pinout (7-pin DIN)
The video pinout is:<br>
- Pin 1 = Vcc (+12V) - only needed for SCART switching, may be left disconnected
- Pin 2 = ground
- Pin 3 = red
- Pin 4 = synch
- Pin 5 = green
- Pin 6 = audio
- Pin 7 = blue

### Input Signals Required
These are based on the Alice schematic - will be changed to reflect MC-10's chip designations, etc.
- SYS_CLK = Z12 pin 12 (74LS14)
- ΦA = Z11 pin 11 (MC6847 VDG)
- ΦB = Z11 pin 10 (MC6847 VDG)
- CHB = Z11 pin 9 (MC6847 VDG)
- Y = Z11 pin 28 (MC6847 VDG)

### Notable Differences Between Alice & MC-10
The crystal for the Alice is located next to the 6803 CPU whereas the MC-10's crystal is part of the RF modulator circuit.  This means that any modification to the MC-10's video output stage needs to include the crystal & system clock generation circuitry ... NOTE TO SELF!

## Status
15-Mar-2025:<br>
Work in progress!<br>
The schematic is almost complete, verifying against the Alice schematic (a bit hard to see some parts) and an actual Alice.<br>
A PCB will then be designed and test PCBs fabricated.
