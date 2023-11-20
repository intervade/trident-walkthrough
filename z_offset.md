---
title: Z Offset Calibration
layout: home
---

# What is Z Offset Calibration?
When the Trident begins a print, it does a couple of things. Among these is auto calibrate the z distance from the probe to the nozzle. When the printer uses the probe, it must know how far the nozzle is in relative distance. Since this process is automated in the start up sequence, it rarely needs to be touched, but occasionally a manual tuning is needed as the auto calibration can only account for so much distance before it errors out.

# How To
First, make sure the z_offset (babystepping) is zero in the movement section. For our measurements to not be impacted by residual filament on the nozzle, heat it to printing temperature. Afterward, home the machine and have it attach the probe with the ATTACH_PROBE macro. Move the toolhead near the middle of the build surface with the movement controls
<img width="470" alt="Screenshot 2023-11-19 at 6 07 28 PM" src="https://github.com/intervade/trident-walkthrough/assets/93929298/7c9ae740-fe25-4d35-a0ad-c173b244baf3">
Then in the console type "probe_calibrate"
<img width="589" alt="Screenshot 2023-11-19 at 6 08 35 PM" src="https://github.com/intervade/trident-walkthrough/assets/93929298/b81eeec8-9a20-45ef-834a-a46aa1d1d74c">
The printer will move toward the bed, clicking the probe twice. It will then move backwards so that the nozzle is over the same spot the probe hit. By hand, remove the probe from the toolhead. Then, a menu on screen will appear for you to move the toolhead down.
<img width="448" alt="Screenshot 2023-11-19 at 6 12 22 PM" src="https://github.com/intervade/trident-walkthrough/assets/93929298/ecfbe9c5-41fb-4135-8a61-86ff150c0c28">
Perform [the paper method] with the menu and a piece of paper. To save, type in "save_config"
<img width="606" alt="Screenshot 2023-11-19 at 6 11 06 PM" src="https://github.com/intervade/trident-walkthrough/assets/93929298/9bcd8567-272c-44c0-b1ff-2616f2f9767d">
The manual offset is done!
