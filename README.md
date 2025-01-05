

<p align="center">
<img alt="enderxy_logo" src="./media/readme_images/enderxy_logo.jpg"></img>
</p>

## Please Read Everything Below Before Contributing, Commenting, or Opening Issues, Thank You!
### This isn't a finished product / refined design. This was a *very* quick concept build and could absolutely use improvement. I hope it can serve as a decent starting point.

# Disclaimer
This project is not affiliated with Creality, Voron Design, Marlin, Mainsail, Klipper, or any other company or project. This is a personal project, and is not intended to be sold or distributed for profit. This project is provided as-is, and I am not responsible for any damage to your printer, or any other equipment. Please accept that when you start this conversion, you cannot change the printer back to stock. By using this project, you agree to take full responsibility for any damage or injury that may occur.

## Skill Level
This project is not for beginners. You should have a good understanding of 3D printing, and be comfortable with modifying and assembling a 3D printer (including drilling, cutting and tapping metal, soldering, etc.). You should also be comfortable with flashing firmware, and configuring it.


# ⚠️ Development Branch Notice

This branch is under active development and contains volatile, experimental changes. Components and designs are frequently updated and may not be synchronized with each other. Specifications, dimensions, firmware, and documentation should be considered unstable and subject to change. For verified, stable content, please refer to the main branch when it is published.

# Ender XY
This is a project to convert a Creality Ender 3 into a CoreXY printer. The goal is to make a good, fast printer from a cheap, slow printer.
- [Contributing](#contributing)
- [TODO's and notes](#todos-and-notes)
- [Klipper](#klipper)
- [Marlin](#marlin firmware)
# Goals
- Make a good printer from a cheap printer
- Keep part cost under $50usd for the conversion
- Use as many stock parts as possible
- Make it easily upgradeable
- Make it easily printable
- Make it easily assembled
- Make it easily sourced

# What to expect
This is a pretty fun build, and in the end you have a good, capable printer. However, 
keep in mind that this is made entirely from a *very cheap printer*. The main advantage is the CoreXY kinematics, which allows for faster print speeds, and less ghosting. It only gets better from there, with the addition of linear rails, a better extruder, and a better hotend, klipper, etc. you can expect to print at a much higher quality, and much, much faster than the stock Ender 3.

## Print specs
So far, on the bone stock conversion, I can reliably print very good quality at 10k acceleration, and around 130mm/s with a .2 layer height. The mk8 extruder really maxes out around 12mm/s^3.

## Specs
Build volume (X,Y,Z):

Linear rail x, V-wheel Y         |     Linear rail x and y
----------------------|-----
 200,185,200          |     200,200,200

## Cost
This will vary wildly with person and location. It's reasonable to assume you can get all the necessary parts for the basic stock conversion (not including the printer), for about $50usd. You'll use a good bit of filament as well.


### The Design
The gantry is an adaptation of a [Voron Trident](https://www.vorondesign.com/voron_trident). Of course, the linear rail version is better, but the V wheel version keeps the cost down, and works great! If you build the v wheel version, you can easily change over to the linear rail version in the future without any modification to the frame or belts. Just attach the rails and swap out the X beam ends.


### The Tool Head
I went with an Afterburner Bowden setup. The files in here allow you to use the stock ender3 hotend in the afterburner, with a 5015 cooling fan. The 5015 fan upgrade is a must for printing PLA fast. The files for the 5015 fan mod are from [Greg191134](https://github.com/Greg191134/Voron/tree/master/Afterburner%20Optimisation/5015%20fan%20mod).

### Filament Feed
Bowden feed is not the greatest, and is a limiting factor as far as print quality and speed are concerned. The upside of running the Bowden is it greatly decreases the mass fo the gantry. If using the stock motors, this is important! Direct drive would be much better, but wouldn't be worth it without A/B motor upgrades. 

## Marlin Firmware

In the firmware directory, you will find two .bin files.One for the stm32 and one for the gd32f. These reflect the configurations found in the marlin configuration files directory. These will only work for:
- Ender3 4.2.2 mainboard with A4988 drivers and stm32 processor
- Ender3 4.2.2 mainboard with A4999 drivers and gd32f processor

### If your board does not match, THE FIRMWARE WILL NOT WORK FOR YOU!
 You need to identify your board and stepper drivers, adjust the configuration files for your build, and build a marlin image. The configuration files needed for marlin 2.x bugfix are in the Marlin_files directory. See [Marlin](https://github.com/MarlinFirmware/Marlin) for more information on how to build your own firmware.


# Klipper
For around $22usd, you can get a raspberry pi zero 2W, and run mainsail with klipper! The Klipper directory has the printer.cfg file for the EnderXY, based on the 4.2.2 mainboard. See [Klipper](https://github.com/Klipper3d/klipper/tree/master) for more info and setup instructions.

# Contributing
I would love to see this project grow, and I would love to see what others can do with it. If you have any ideas, improvements, or requests, please feel free to open an issue, or, fork the project and make a pull request.

# Before you Contribute, Please Read!
### It's easy to just throw money at this, to add better parts and make it a better printer. That's not the point of this project, and it's what makes it a challenge. The point is to make a good printer from a cheap printer, using as many stock parts as possible.
### If you have a suggestion, please consider the cost and the availability of the parts. If you have a design change, please consider the ease of printing and the ease of assembly.
### If you have a request, please consider the goals of the project, and the limitations of the stock parts.

## TODO's and notes
    - BOM needs completed, and to include different configurations
    - optmize part designs for printing without support
    - Ndesigns for linear rail Z axis
    - designs for three Z motors and leadscrews

# Sources and mentions
The only reason this project was possible, and frankly, why I was able to create the first concept so quickly, is because of awesome open source projects! I don't want anyone to think that I did something amazing here, I simply adapted what I could from others, and made a few parts that weren't out there yet.

Of course [Voron Design](https://vorondesign.com/). An amazing, very generous engineering team.

[Marlin](https://github.com/MarlinFirmware/Marlin), Making the maker world a better place.

This wonderful person [Greg191134](https://github.com/Greg191134) is the source of the 5015 fan mod for the afterburner: [Afterburner 5015 fan mod](https://github.com/Greg191134/Voron/tree/master/Afterburner%20Optimisation/5015%20fan%20mod). They also have an awesome project called the Vorender-4, where they upcycled an ender 4 with an adaptation of the Trident gantry. 
