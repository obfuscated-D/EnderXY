
## Please Read Everything Below Before Contributing, Commenting, or Opening Issues, Thank You!
### This isn't a finished product / refined design. This was a *very* quick concept build (we're talking < 8hrs quick), and could absolutely use improvement. I hope it can serve as a decent starting point.

# ⚠️ Development Branch Notice

This branch is under active development and contains volatile, experimental changes. Components and designs are frequently updated and may not be synchronized with each other. Specifications, dimensions, firmware, and documentation should be considered unstable and subject to change. For verified, stable content, please refer to the main branch when it is published.

# The firmware is not up to date!!!!!!!!!!!!!!!!!!

# Ender XY
This is a project to convert a Creality Ender 3 into a CoreXY printer. The goal is to make a good, fast printer from a cheap, slow printer.
- [Contributing](#contributing)
- [TODO's and notes](#todos-and-notes)

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
keep in mind that this is made entirely from a *very cheap printer*. With no upgrades to the motors,extruder, or a linear rail conversion, you can expect to print at about the same quality as the stock Ender 3. The main advantage is the CoreXY kinematics, which allows for faster print speeds, and less ghosting. It only gets better from there, with the addition of linear rails, a better extruder, and a better hotend, you can expect to print at a much higher quality, and much, much faster than the stock Ender 3.

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

## Firmware
## The firmware is not up to date, DO NOT USE IT!!!!!!!!!!!!!!!!!!
There is a ready to go firmware.bin in the firmware folder for a build with the following configuration:
- Creality 4.2.2 main board with the STM32F103 processor
- A4988 stepper drives
- Linear rail X
- Afterburner bowden
- Factory extruder
- Factory hotend
- V-wheel Y
- V-wheel Z

### If your build or board does not match this configuration THE FIRMWARE WILL NOT WORK FOR YOU!
 You need to identify your board and stepper drivers, adjust the configuration files for your build, and build a marlin image. The configuration files needed for marlin 2.x bugfix are in the Marlin_files directory. See [Marlin](https://github.com/MarlinFirmware/Marlin) for more information on how to build your own firmware.


# Contributing
I would love to see this project grow, and I would love to see what others can do with it. If you have any ideas, improvements, or requests, please feel free to open an issue, or, fork the project and make a pull request.

# Before you Contribute, Please Read!
### It's easy to just throw money at this, to add better parts and make it a better printer. That's not the point of this project, and it's what makes it a challenge. The point is to make a good printer from a cheap printer, using as many stock parts as possible.
### If you have a suggestion, please consider the cost and the availability of the parts. If you have a design change, please consider the ease of printing and the ease of assembly.
### If you have a request, please consider the goals of the project, and the limitations of the stock parts.

## TODO's and notes
    - BOM needs completed, and to include different configurations
    - Configuration files need to be updated
    - Firmware needs to be updated
    - Need to optmize part designs for printing without support
    - Need to add designs for linear rail Z axis
    - Need to add designs for three Z motors and leadscrews

# Sources and mentions
The only reason this project was possible, and frankly, why I was able to create the first concept so quickly, is because of awesome open source projects! I don't want anyone to think that I did something amazing here, I simply adapted what I could from others, and made a few parts that weren't out there yet.

Of course [Voron Design](https://vorondesign.com/). An amazing, very generous engineering team.

[Marlin](https://github.com/MarlinFirmware/Marlin), Making the maker world a better place.

This wonderful person [Greg191134](https://github.com/Greg191134) is the source of the 5015 fan mod for the afterburner: [Afterburner 5015 fan mod](https://github.com/Greg191134/Voron/tree/master/Afterburner%20Optimisation/5015%20fan%20mod). They also have an awesome project called the Vorender-4, where they upcycled an ender 4 with an adaptation of the Trident gantry. 
