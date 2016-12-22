# Original Prusa i3 MK2 Helpful Info
These are mostly a collection of notes for myself about my Original Prusa i3 MK2 3D Printer, but maybe you'll find them useful.

# Zip Ties
Major :key:

# Supplemental Printed Parts
## 3-Point Y-Axis Motor Mount
The stock motor mount flexes quite a bit with tension on the Y-Axis belt. I swapped it for a 3-point which is much sturdier and doesn't allow the motor to flex much.

## Y-Axis Brace
Printed this and attached to frame while assembling, then removed later. Helped to keep the Y-Carriage square.

## P.I.N.D.A Probe Protector
The PINDA probe is quite low, not too much higher than the nozzle. In the rare instance that a print raises up, it's possible that the PINDA protector could get damaged. Printing a probe protector helps keep the PINDA protected just in case. *This must be printed in ABS due to the part's close proximity to the nozzle.*

# First Calibration
Make sure to sit by the printer and have a sheet of paper on the PEI surface while running the first 4 points of the XYZ calibration. I had incorrectly mounted my PINDA probe, walked away, and came back to a damaged PEI sheet.

# PID Tuning
Must PID tune after swapping nozzles. An overview of PID Tuning can be found [here](reprap.org/wiki/PID_Tuning).

## PID Autotune w/ Marlin Firmware & OctoPrint
Thomas Sanladerer has a great tutorial [here](https://www.youtube.com/watch?v=APzJfYAgFkQ).

# Slic3r
## Configuration files
On Mac OSX, they're stored in the directory: `/Users/<USERNAME>/Library/Application Support/Slic3r`
On Windows, they're stored in the directory: `C:\Users\Public\Documents\Prusa3D`.

I found myself wanting to wipe these out a few times and start over with new config bundles, so I thought this was handy to place here.
