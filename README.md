# Internal 4KB-to-8KB RAM Upgrade
This design is based on the work that Daniel Tufvesson documented on his [blog](https://www.waveguide.se/?article=expanding-the-trs-80-mc-10-internal-ram) for the Tandy TRS-80 MC-10. Please refer to his blog for the background and theory of the upgrade.<br>

I have [tested it on my Alice](https://youtu.be/OvdkhOnV7no) but not yet (as of 27-Feb-2025) on my MC-10.<br>

Standard Alice 4KB: 3142 bytes free<br>
Alice with 8KB: 7238 bytes free<br>

![Alice free memory with 8KB RAM](/Internal_8KB_RAM/Alice_8KB_free_mem.png)

The MC-10 has a limitation with component height due to its rather [snug FCC shielding](https://www.waveguide.se/?article=getting-to-know-the-trs-80-mc-10) - the Matra Alice doesn't have this, hence this simple daughterboard design.  My MC-10 no longer has that limitation either!<br>

The Alice also doesn't have the bodge wiring for the 4KB address decoding that the MC-10 has.<br>

This is what the 8KB daughterboard looks like installed in the Alice:<br>

![Internal daughterboard installed in Alice](/Internal_8KB_RAM/Matra_Alice_8KB_installed.jpeg)

(Sidenote 1: yes, the crossing of the black and yellow 6847 VDG address wires annoys me too - I have since updated the PCB so they don't cross!)<br>

(Sidenote 2: the original Thomson 6803 CPU in my Alice was faulty causing keyboard issues - I replaced it with a socketed Motorola 6803 seen on the left).<br>

On the MC-10 it is necessary to also move a bodge wire from A12 (6803 pin 25) to A13 (6803 pin 24).  On the Alice this simply requires cutting a track to pin 25 and connecting it to pin 24:<br>

![Alice bodge wire relocation](/Internal_8KB_RAM/Z1_6803_pin25_to_pin24.jpeg)



