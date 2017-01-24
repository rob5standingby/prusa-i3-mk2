# Original Prusa i3 MK2 Guide

## Overview
This repository serves as my personal notebook for assembly, calibration, operation, maintenance and improvement of the Original Prusa i3 MK2. I hope you also find it useful.

### Table of Contents
- [I. Assembly](#i-assembly)
- [II. Calibration](#ii-calibration)
- [III. Printing](#iii-printing)
- [IV. Maintenance](#iv-maintenance)
- [V. Troubleshooting](#v-troubleshooting)
- [VI. Software](#vi-software)
- [VII. Useful GCode](#vii-useful-gcode)
- [VIII. Additional Resources](#viii-additional-resources)

## I. Assembly
The best resource for assembly is the [official assembly instructions](http://manual.prusa3d.com). However, before assembly, I recommend that you read this small section.

### Tools
The Original Prusa i3 MK2 kit includes all of the tools necessary to assemble the printer. However, there are a few additional tools that will make your life easier when assembling.

| Name         | Purpose |
| :----------- | :------ |
| Calipers (8-inch or greater) | A precise machine requires precise assembly. Large calipers will help you to make sure everything is properly positioned during assembly. |
| [Loctite (Blue)](https://www.amazon.com/Loctite-Blue-Threadlocker-6-Milliliter-209728/dp/B000I1RSNS) | The PINDA calibration probe requires 2 nuts to fasten it to the hotend assembly. It is important that this probe remains in place. After you've assembled the printer and it has been running successfully for a few days, you should apply a small drop of blue Loctite. |

### Extra Printed Parts
There are a few parts not included from Prusa that you should print. These parts will aid in your assembly of the printer. Descriptions, sources, material recommendations, and printing settings can be found in each entry in the table below. If you don't already have a 3D Printer, you can find a local person to print these for you. My recommended way of locating someone local is to use the [3D Hubs](http://www.3dhubs.com/) service.

| Name   | Purpose | Material | Settings | STL     | Source  |
| :----- | :-----  | :-----   | :-----   | :-----  | :------ |
| **3-Point Y Motor Holder** | This model is a drop-in replacement for the Y-Motor holder which is included in the Original Prusa i3 MK2 kit. can be substituted during assembly The stock Y-motor holder design attaches to only two of the 4 attachment points of the NEMA 17 stepper motor. In my experience, when the belt for the Y-Axis is tensioned, the stock motor mount flexes quite a bit. This could possibly cause additional strain on the stepper motor shaft and cuase it to fail sooner. Adding an extra contact point to the motor mount affords the motor greater rigidity and less flex. | ABS is recommended because of its mechanical properties. However, this part could be printed in PLA or PETG as well. | 3 Perimeters, 30% Triangle Infill, 4/4 Top/Bottom layers | TODO | [Thingiverse](http://www.thingiverse.com/thing:1837853) |
| P.I.N.D.A Probe Protector | The PINDA calibration probe sits at a very low height in the Z-direction, not much higher than the hotend nozzle. In rare instances, a print can "curl" up. This protector prevents damage to the calibration probe if curling ever occurs. Assembly instructions for this part can be found in the [official assembly instructions](http://manual.prusa3d.com). | Due to its proximity to the hotend, this must be printed in ABS or a material with similar high-temp  resistant properties | 100% infill recommended | TODO |   [Prusa3D](http://www.prusa3d.com/prusa-i3-printable-parts/) |
| Y-Frame Assembly Helper | While the Original Prusa i3 MK2 can compensate for a skewed printer assembly, its best to assemble everything square to begin with. This part aids in assembly by snapping to the 8MM threaded rods in the Y-stage assembly during construction. This part can be zip-tied to the threaded rods, or removed later on. | ABS/PETG/PLA | 3 Perimeters, 20% infill, 4/4 Top/Bottom layers | [STL] | [Thingiverse](http://www.thingiverse.com/thing:1846654) |
| P.I.N.D.A Calibration Tool | Arguably one of the most frustrating parts of getting the Original Prusa i3 MK2 calibrated properly is getting the Z-Height of the PINDA Calibration Tool Correct. | Any | 2 perimeters, 20% infill, 4/4 Top/Bottom Layers | [STL] | [NERDVille's Thingiverse](www.thingiverse.com/thing:1977997) |
| [name] | [purpose] | [material] | [settings] | [STL] | [source] |

## II. Calibration
**Please read this section in its entirety before ever turning the Original Prusa i3 MK2.** It is **imperative** that you follow these instructions and the Prusa Manuals in order to prevent damage of your printer. The printing manual included with the Original Prusa i3 MK2 has a very handy diagram on the calibration flow of the machine. My intention with this section is to strongly reinforce some instructions that are in the Prusa Manual.

### PINDA Probe Height Adjustment
Once you have passed the machine's self-test, calibrate the height of the PINDA Probe using the PINDA Calibration tool that you printed above. Failure to have the PINDA probe at the optimal height will result in a failed XYZ Calibration and lots of headaches. The steps of this adjustment process are outlined in the table below.

| Step # | Description |
| :----- | :---------- |
| Step 1 | **ENSURE BOTH THE PRINTER NOZZLE AND THE HEATED BED ARE AT ROOM TEMP**. |
| Step 2 | Place the PINDA calibration tool in the center of the heated bed |
| Step 3 | Using the click-wheel on the |

*TODO* Finish this documentation.

### XYZ Calibration
Once you have adjusted the height of the PINDA probe using the calibration tool above, you're ready to perform the XYZ calibration. **IMPORTANT:** The full XYZ calibration process can take approximately 10 minutes. It is VERY important that you babysit the printer and do not leave it unattended during this process. Follow the Prusa instructions precisely. Use a sheet of paper on the print surface while running the calibration. If the nozzle drags the piece of paper and causes it to move, IMMEDIATELY turn off the printer. If you have properly set the height of the PINDA probe, you should have absolutely no issues with this process. Learn from my mistakes! During assembly of my first printer, I had incorrectly set the height of the PINDA probe. I clicked "XYZ calibration" and walked away, and came back to the printer digging itself into the print bed, causing irreversible damage to the PEI surface.

### Calibration V2 (Live-Z Adjustment)
Hopefully, the XYZ calibration succeeds first go, anad you're nearly ready to print!! The next step in the calibration process is fine-tuning the height of your hotend nozzle in relation to the print surface. The feature of the Original Prusa i3 MK2 that you'll be utilizing for this adjustment is called "Live-Z Adjustment." This setting persists once you've set it, but you will find yourself using this feature occasionally to make fine-tuning tweaks after changing material types, or after you've changed nozzles.

### Z-Calibration
The Z-Axis can be calibrated independently of the entire XYZ process. This process is much faster. If you ever pick up the printer and move it, or manually adjust the Z-height of the printer by rotating the threaded rods on the Z-Axis, you'll need to re-run the Z-Calibration before printing again.

## III. Printing
> A watched print never fails. -My Grandma

### Before You Print
Follow this general checklist before you print to ensure a successful print.

- [ ] **If the printer has been moved since last print**, re-run the "Z Calibration" from the Prusa LCD while the printer is still cold.
- [ ] Hotend/Nozzle area is free of filament "boogers" or "ooze".
- [ ] Heated Bed is properly cleaned. Isopropyl Alcohol and a Paper Towel is a good cleaning method.
- [ ] Verify there is nothing obstructing the printer in the X, Y, or Z axes.

### When You Print
**The First Layer: Adhesion and Proper Live Z-Height**
Having proper adhesion of your first layer is critical to having a successful print. You want the first layer to adhere enough to the print bed so that the object will stay in place during printing, but not stick so well that you cannot remove it later on. Different materials require more or less "squish" of the filament to the print surface. Watch the printer very carefully during the first layer. If you see an air gap between "lines" of filament, your nozzle may not be close enough to the print bed. You can adjust the height of the nozzle during printing using the "Live Z Adjust" feature of the printer.

Keep an eye on the printer during the first layer. If things start to peel up during this time, you likely have a setting wrong, and you should stop the print and try again.

### After Your Print Finishes
**Removing your object from the print bed**
**IMPORTANT** The PEI sheet can be damaged if you do not take proper precautions when removing prints from the printer. Follow these steps and you won't risk causing damage to the print surface.

- Wait for the nozzle and the heated bed to cool to room temperature.
- Gently slide your 3D Printer Spatula tool under a corner of the print. Try to avoid any "prying" action, as this could cause damage to the print bed. Keep the tool as parallel to the print surface as possible. 
- Slowly work the spatula around various sides of the print.
- If you're having trouble finding a good 'corner' to start with, you may want to try using a piece of dental floss.
- After removing a print, you may notice an outline of your printed object in the PEI sheet, or some small bubbles. This is completely normal and will go away with time.


## IV. Maintenance
The following maintenance should be performed after printing with approximately one spool (or 1KG) of filament.

## V. Troubleshooting
*TODO* Fill this out...

## VI. Software
*TODO* Fill this out...

## VII. Useful GCode
*TODO* Fill this out...

## VIII. Additional Resources
http://www.prusa3d.com/material-guides/ (Tips for printing on the MK2 with various materials)
https://github.com/PrusaMK2Users/MK2_Tips_and_Tricks/wiki
https://github.com/PrusaMK2Users/MK2_Tips_and_Tricks

## PID Tuning
After changing nozzles in your hotend, you must PID tune. If you'd like to know more about what PID tuning is, you can read about it [here](reprap.org/wiki/PID_Tuning) on the RepRap wiki.

### PID Autotune w/ Marlin Firmware & OctoPrint
If you're running OctoPrint, you can run the "Autotune" in Marlin from the console in your browser. Thomas Sanladerer has a great tutorial [here](https://www.youtube.com/watch?v=APzJfYAgFkQ).

## Slic3r (PRUSA EDITION)
### First Run (macOS)
Upon first run of Slic3r (PRUSA EDITION) you'll be prompted with a wizard to setup your printer. Click cancel. You'll now want to load the config bundle by going to `File > Load Config Bundle` and selecting the correct `.ini` file that was included with the Prusa Drivers.

### Configuration files
I found myself wanting to delete the preset data in Slic3r after importing tons of config bundles that I didn't really want, and wanting to re-import all of the config data again after making modifications to the .ini files. This is how you find that stuff ;).

### macOS
Running slic3r from the terminal using the command: `/Applications/Slic3r.app/Contents/MacOS/slic3r --debug` will output the directory where your data is stored.

### Windows
Check either `C:\Users\Public\Documents\Prusa3D` or `C:\Users\Public\Documents\Prusa3D\Slic3r settings MK2\printer`

## OctoPi/OctoPrint
If you setup OctoPrint to run w/ the Prusa MK2, create a printer profile and use the following settings:
- Heated Bed: [y]
- Print Volume:
  - Width (x): 250mm
  - Depth (y): 210mm
  - Height (z): 200mm
- Custom bounding box: [y]
  - X Coordinates: Min: 0, Max: 250
  - Y Coordinates: Min: -4, Max: 210
  - Z Coordinates: Min: 0, Max 200

The "Custom Bounding Box" is for the 'purge strip' that the printer prints out.

Prusa i3 MK2 details
  -   heated bed
- calibration probe

Before your first print
- COLD NOZZLE for XYZ Calibration

Navigating the Marlin Firmware via LCD

Before you print checklist
- Have you moved the printer ? Rerun the "z calibration"
- Check the nozzle for any debris. Use a wire brush to gently remove any plastic.
- Check the bed for any debris. Clean with isopropyl alcohol and a dry paper towel
- Check the thermistor wiring under the heat block
- Check the z threaded rods. Ensure no debris is there.

Maintenance (Every Few months)
- Check tightness of belts
- Check pulley set screws on X and Y motors


Upgrades
- Fancy filaments need fancy nozzles !!!
- PID tuning

Troubleshooting
- adhesion issues
