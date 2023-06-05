---
title: Printing
layout: home
---

# Printing
## We need a file to print
Often, we have to get the file from Solidworks to a slicer, in our case PrusaSlicer. In order to do this, the file must be exported in a supported format, the most popular of which is STL. Navigate to File > Save As, then select STL under file type.
![solidworks_saving](https://github.com/intervade/trident-walkthrough/assets/93929298/de2ab380-d033-4f86-bed8-2f412e22418d)

## I don't want to make the file
Understandable, modeling everything can get tedious. You can try to find something that'll fit your needs from websites like [thingiverse] or [printables], among other websites you can search for on google. Check the license to know if you can use it for research or only for personal use.

## First time slicer setup
This includes setting up profiles for both the Aquila and the Trident, since it can be done together. [If the computer you're going to use to slicer the file has not set it up yet, click here].

## Slicer time
Now, with the file, we start in the slicer. Rather than start from zero, [read this page from the developers' website] to get a general overview of what's going on. However, ignore the brim section, we seldom need those. If you find yourself wanting to fine tune how the printer functions in the future, that website has excellent documentation on all of the settings can that be tweaked, but in general you won't have to. Since Dr. Chen has two printers, it's important to select the profile corresponding to the machine you're going to use. Additionally, check the filament profile matches the filament type you are using.
![prusaslicer_quicksettings](https://github.com/intervade/trident-walkthrough/assets/93929298/06a69dad-b21b-44e1-b17e-9979647063ca)

Under Print Settings, the number before the name of the profile specifies the layer height of the print. 0.2mm is a good balance of speed and quality, being the most common option. For extra resolution, make the layer height smaller, but to have the print go faster, try a greater layer height.

## Utilizing the file
After you are able to import the STL file and click slice, a gcode file will be generated. **Regardless of the machine, make sure the nozzle is clean before starting the print job.** Sometimes the filament has a hard time getting started when there's excess hanging around.

### For the Aquila,
you must save the file to a micro SD card that will be put into the front of the machine. Using the LCD screen with the rotary knob, select the print option, navigating to the file you made and selecting it. The machine will heat the bed, then the hotend, and begin the print.

### For the Trident,
you must save the file to your computer. Afterward, nagivate to your computer's WiFi settings, changing to "klipper". In a browser, enter 10.42.0.1 as a URL, which will take you to the web interface for the Trident.
![wifi_selection](https://github.com/intervade/trident-walkthrough/assets/93929298/38bb6363-4fb6-4f92-bbc1-ff4ae6db8b5c)

For the Trident it is important to let the machine reach printing temperatures by entering the same values from the PrusaSlicer "Filament Settings" tab and heat soak for at least 10 minutes before running the gcode. Since the bed is a thick, 6mm sheet of aluminum, it takes time for the whole plate to reach temp, during which thermal expansion is occuring. Although the expansion is small, with layers 0.2mm thin, it is pertinent.
![temp_setting](https://github.com/intervade/trident-walkthrough/assets/93929298/4c3bfbea-9653-4508-80a7-9cf7c07be171)
These temps are examples of setting the printer for PLA, although your temps may not match exactly.

Scrolling down, there is a section titled "Jobs". Click the "+" symbol, subsequently uploading the gcode you saved.
![file_uploading](https://github.com/intervade/trident-walkthrough/assets/93929298/2e9cf87e-b678-4bd1-9a82-09f5d2e124b6)

After waiting for the printer to reach temperature and soak, click the file you uploaded in the Jobs section and select the print file option.
![print_start](https://github.com/intervade/trident-walkthrough/assets/93929298/ccc090c1-5f40-4c2f-9996-e2529bb2477b)

[read this page from the developers' website]: https://help.prusa3d.com/article/first-print-with-prusaslicer_1753
[If the computer you're going to use to slicer the file has not set it up yet, click here]: https://intervade.github.io/trident-walkthrough/slicer_setup.html
[thingiverse]: https://www.thingiverse.com
[printables]: https://www.printables.com
