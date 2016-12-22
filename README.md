# Original Prusa i3 MK2 Helpful Info
These are mostly a collection of notes for myself about my Original Prusa i3 MK2 3D Printer, but maybe you'll find them useful.

## Zip Ties
Major :key:

## Supplemental Printed Parts
### [3-Point Y-Axis Motor Mount](http://www.thingiverse.com/thing:1837853)
The stock motor mount flexes quite a bit with tension on the Y-Axis belt. I swapped it for a 3-point which is much sturdier and doesn't allow the motor to flex much. *Print in ABS*

### [Y-Frame Assembly Helper](http://www.thingiverse.com/thing:1846654)
Printed this and attached to frame while assembling, then removed later. Helped to keep the Y-Carriage square.

### [P.I.N.D.A Probe Protector](http://www.prusa3d.com/prusa-i3-printable-parts/)
The PINDA probe is quite low, not too much higher than the nozzle. In the rare instance that a print raises up, it's possible that the PINDA protector could get damaged. Printing a probe protector helps keep the PINDA protected just in case. *This must be printed in ABS due to the part's close proximity to the nozzle.*

## First Calibration
Make sure to sit by the printer and have a sheet of paper on the PEI surface while running the first 4 points of the XYZ calibration. I had incorrectly mounted my PINDA probe, walked away, and came back to a damaged PEI sheet.

## PID Tuning
After changing nozzles in your hotend, you must PID tune. If you'd like to know more about what PID tuning is, you can read about it [here](reprap.org/wiki/PID_Tuning) on the RepRap wiki.

### PID Autotune w/ Marlin Firmware & OctoPrint
If you're running OctoPrint, you can run the "Autotune" in Marlin from the console in your browser. Thomas Sanladerer has a great tutorial [here](https://www.youtube.com/watch?v=APzJfYAgFkQ).

## Slic3r (PRUSA EDITION)
### First Run (macOS)
Upon first run of Slic3r (PRUSA EDITION) you'll be prompted with a wizard to setup your printer. Click cancel. You'll now want to load the config bundle by going to `File > Load Config Bundle` and selecting the correct `.ini` file that was included with the Prusa Drivers.

### Configuration files
I found myself wanting to delete the preset data in Slic3r after importing tons of config bundles that I didn't really want. This is how you find that stuff ;).

### macOS
Running slic3r from the terminal using the command: `/Applications/Slic3r.app/Contents/MacOS/slic3r --debug` will output the directory where your data is stored. 

### Windows
They're typically stored in the directory: `C:\Users\Public\Documents\Prusa3D`.
