![How it looks](https://github.com/ezcGman/n64-denc-nus-adapter/blob/master/castellated/pictures/N64-DENC-NUS-Adapter-Castellated-render-front.png?raw=true)

# N64 DENC-NUS Adapter
This PCB is a soldering / modding help to any N64RGB mods that need to solder wires to the tiny (1.27mm) spaced DENC-NUS display IC, like [Tim Worthington's N64RGB mod](http://etim.net.au/n64rgb/). It is also a 1-layer board, so it has nothing on the board's bottom side, to not risk any shorts with the vias on the N64 mainboard.

If you have a MAV-NUS adapter, most mods already come with an adapter / flex-PCB, so I'm not offering those.

## Board versions
There are two versions in this repo:
* One has castellated holes (half holes at the PCBs edge), which is definitely the best and easiest to solder, as it just "snaps in" nicely to the DENC-NUS. However, castellated holes are more expensive when printing at e.g. JLCPCB or PCBWay.
* The other one has simple [SMD pads spaced 0.2mm from the PCBs edge](https://github.com/ezcGman/n64-denc-nus-adapter/blob/master/smd/pictures/N64-DENC-NUS-Adapter-SMD-traces-front.png), which is the minimum for both JLCPCB and PCBWay. Printing this version will not generate any extra cost, so you can get it for the usual $2 or $5.

## Printing instructions
### Both JLCPCB and PCBWay and both board versions
* *(If not already pre-selected)*: Select 1-layer board
* Select 0.8mm as board thickness (this should still be $2 / $5)
* Select whatever you want for PCB color, silkscreen, surface finish, etc.

### Castellated holes version
* Select "Castellated Holes: Yes". PCBWay hides this under "Advanced PCB"

### JLCPCB
* Select "Remove Order Number: Specify a location". I have a placeholder so the order number ends up in a corner. This won't cost you extra.

## Parts list
None are required, but the SMD pads are designed to either solder wires directly, or use a left-right SMD pin header:

* 1x 12-pin 2.0mm **(!!)** left-right **angled** SMD pin header *(optional)*
    * If you cannot find an angled pin header, get a straight one and bend the pins yourself

## Tools list
### Required
- A soldering iron
- Soldering tin
- Double-sided tape

## Installation
No matter which version (castellated or SMD), the steps are really straightforward:
1. Put some double sided tape on the bottom side. This isn't neccessarily required, but holds it the PCB in place when soldering it to the DENC-NUS
2. Put it down as close to the DENC-NUS as possible. Pay attention that the pads are properly centered to the pins of the DENC-NUS
![Board glued down](https://github.com/ezcGman/n64-denc-nus-adapter/blob/master/install-pictures/1.jpg?raw=true)
3. Choose a thin-ish tip on your soldering iron (like a 1mm round head) and solder each pin to the board. Use very little tin, otherwise you risk a bridge
![Microscope view](https://github.com/ezcGman/n64-denc-nus-adapter/blob/master/install-pictures/2.jpg?raw=true)
4. Multimeter that you have not created any bridges / shorts
5. Solder the wires that usually should go directly to the DENC-NUS now to the nicely spaced SMD pads (the ones on the bottom in the above picture) :) 
    * Alternatively, if you decided to go with a pin-header, solder it to the SMD pads
6. Continue with the install instructions of the mod you're using

## KiCad dependencies
*(Only required if you want to edit the PCb in KiCad)* It might happen that KiCad is missing my custom footprints. You can find and download them here and then add them to KiCad: https://github.com/ezcGman/andys-footprints

## Credits
As for all my PCBs: Huge thanks to Quindor from QuinLED.info and also the folks from #pcb-design-talk on his Discord server! Would not have been able to do anything without these people!!
