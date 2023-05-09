---
title: Aquila
layout: home
---

# [Voxelab Aquila X2]
This is an entry level machine. Quick description
- The link above is for the website, which can be helpful
- Voxelab is the company, which is a subsidary of Flashforge
- Aquila is the base design, of which there are a couple of iterations
- X2 is our specific model

## Summary...ish
- Similar motion concepts
- Bed leveling is manual
- Extrusion is slightly sloppier
- **Be careful with hotend temperature**
- Swap slicer profile to Ender 3 V2

## Let's go through it
Although basic, can get most jobs done! However, it will be a little slower.

### Basics
The motion system works in the same XYZ plane, with the E axis for extrusion. In a similar manner to the trident, the X and Y are moved by toothed belts, and the Z is moved by a leadscrew.
The filament is pushed by a gear. The X carriage is the hotend assembly on the horizontal rail. The Y carriage is the heated bed that moves back and forth. The Z axis is the X gantry moving up and down.

### Motion
Belt tension is still important, but having the X and Y be the exact same is not as vital. Each simply has to be in the sweet spot of not floppy yet not tightly pulled. Otherwise, instead of the X and Y motors
working together, each axis has its own dedicated motor. Still, each has a pulley and bearing at the opposing end. The Z axis works the exact same, only with one screw instead of three. The Z axis is then
cantilevered. If the wheels are properly tightened, this is not an issue. Make sure that the motor for the Z has a little play, as well as the nut. The components on entry printers are cheap, so the leadscrews
are often imperfect. This is remedied by introducing slight play so that the imperfections are not translated into the Z motion. This is not a dealbreaker, as in the printer won't stop working, but it does make
a noticable quality difference. Each axis has a simple endstop switch to take them to the homing position of (0, 0, 0).

### Bed Leveling/Tramming
On the trident, bed inconsistencies and leveling are taken care of automatically. This is a more advanced feature not found on the aquila. Therefore, the bed must be leveled. [The paper method works well for this
machine.] This does not need to be done often.

### Extrusion System
The trident uses a direct drive setup, while the aquila uses a bowden. Both have a long PTFE tube for filament guidance. The difference is that the trident pulls the filament through, since the E motor is on the
moving toolhead, but the aquila *pushes* the filament through the tube, since the E motor is decoupled from the toolhead. It is instead on the Z gantry. While both systems work, the bowden setup does not provide
as much control over the filament. This results in longer retractions, and usually only results in some surface imperfections. However, nothing major.

### Hotend
The hotend functions the same. There is the heatsink, the heatbreak, heat block, heater cartridge, thermistor, and nozzle. **This machine does not have an all-metal heatbreak. The PTFE tube feeds all the way down through the heatbreak into
the heaterblock. This means that the PTFE gets as hot as the nozzle does. PTFE offgasses at higher temps, and while there is discourse on exactly what temps are safe, I never run hotter than 235.** Additionally, it
does not have the same volumetric flow, but that doesn't matter since this machine does not print as fast as the trident does.

### Fans
There are three fans on the machine. One is a 4010 fan for the heatsink. Another is a 4010 *blower* fan for part cooling from the right side of the nozzle. The last is a 4010 to cool the electronics. The two
normal 4010 fans are wired to be always on. The blower is controlled by the slicer settings.

### Mainboard
Hopefully, you don't really touch the mainboard, unless something bad happens. It's not insanely difficult to mess with, but it can seem daunting. There is a picture of the board on the Voxelab aquila page. The board is nicely labeled, both on the silk screen and with little ties
around the wires.

### Control
All the controls for the printer come from using the screen's rotary knob. The files are printed from the micro SD card that's inserted.

### Slicer
You can also use PrusaSlicer for this machine. Just swap the default settings from anything voron related to Ender 3 V2. The Creality Ender 3 V2 is the machine that the aquila is based upon, almost being an exact
clone. As such, the printing profiles will work perfectly. Instead of saving the file to your computer and uploading it, instead save it to the SD card that is put into the machine.


[Voxelab Aquila X2]: https://www.voxelab3dp.com/product/aquila-x2-fdm-3d-printer?cID=31
[The paper method works well for this machine.]: https://www.tomshardware.com/how-to/level-3d-printer-bed
