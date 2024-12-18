
## Please Read Everything Below Before Contributing, Commenting, or Opening Issues, Thank You!
### This isn't a finished product / refined design. This was a *very* quick concept build (we're talking < 8hrs quick), and could absolutely use improvement. I hope it can serve as a decent starting point.

# ⚠️ Development Branch Notice

This branch is under active development and contains volatile, experimental changes. Components and designs are frequently updated and may not be synchronized with each other. Specifications, dimensions, firmware, and documentation should be considered unstable and subject to change. For verified, stable content, please refer to the main branch when it is published.

# The firmware is not up to date!!!!!!!!!!!!!!!!!!

# Ender XY
This is a project to convert a Creality Ender 3 into a CoreXY printer. The goal is to make a good printer from a cheap printer, using as many stock parts as possible, and to make it easily upgradeable.
- [Contributing](#contributing)
- [TODO's and notes](#todos-and-notes)

# Goals
- Make a good printer from a cheap printer
- Keep cost under $50usd for the most basic conversion
- Use as many stock parts as possible
- Make it easily upgradeable
- Make it easily printable
- Make it easily assembled
- Make it easily sourced

# What to expect
This is a pretty fun build, and in the end you do have a working, capable printer. However, 
keep in mind that this is made entirely from a *very cheap printer*. With no upgrades to the motors,extruder, or a linear rail conversion, it's not going to be a rapid, production level machine like a Bambu or a Voron. This is more so a project for the love of the build. 

## Specs
Build volume (X,Y,Z):

Linear rail x, V-wheel Y         |     Linear rail x and y
----------------------|-----
 200,185,200          |     200,200,200

## Cost
This will vary wildly with person and location. It's reasonable to assume you can get all the necessary parts for the basic stock conversion (not including the printer), for about $50usd. You'll probably use most of a 1kg spool of filament as well.

## Design
The overall idea was to turn a cheap ender 3 into a good platform for an easily upgradeable, affordable, core xy machine, incorporatating as many stock components as possible to reduce the BOM.

You can use all the bone stock components and a very small list of extra materials, and make a functional corexy that prints faster than a stock ender 3. This allows easy incremental upgrades such as changing to direct drive extruders, larger stepper motors etc.


### The Gantry
The gantry is essentially a modified Trident gantry, and there are two versions in here, there is the v-wheel version, and the linear rail version. Of course, the linear rail version is better, but the V wheel version only needs some bolts and some printed parts, and it works fine. If you build the v wheel version, you can easily change over to the linear rail version in the future without any modification to the frame or belts. Just attach the rails and swap out the X beam ends. 

The V wheel version does limit the Y axis to 185mm, with the linear rail version you can get the full 200. 

### The Tool Head
I went with an Afterburner Bowden setup, The files in here allow you to use the stock ender3 hotend in the afterburner, and a 5015 blower fan. If using the linear rail X version, any of the voron tool heads should fit.

### Filament Feed
Bowden feed is not the greatest, and is a limiting factor as far as print quality and speed are concerned. The upside of running the Bowden is it greatly decreases the mass fo the gantry, if using the stock motors, this is important! Direct drive would be much better, but wouldn't be worth it without A/B motor upgrades. 

## Firmware
There is a ready to go firmware.bin in the firmware folder for a build with the following configuration:
- Creality 4.2.2 main board
- A4988 stepper drives
- Linear rail X
- Afterburner bowden
- Factory extruder
- Factory hotend
- V-wheel Y
- V-wheel Z

### If your build does not match this configuration THE FIRMWARE WILL NOT WORK FOR YOU!
 You need to identify your board and stepper drivers, adjust the configuration files for your build, and build a marlin image. The configuration files needed for marlin 2.x bugfix are in the Marlin_files directory. See [Marlin](https://github.com/MarlinFirmware/Marlin) for more information on how to build your own firmware.


# Contributing
I would love to see this project grow, and I would love to see what others can do with it. If you have any ideas, improvements, or requests, please feel free to open an issue, or, fork the project and make a pull request.

# Before you Contribute, Please Read!
### It's easy to just throw money at this, to add better parts and make it a better printer. That's not the point of this project, and it's what makes this project difficult. The point is to make a good printer from a cheap printer, using as many stock parts as possible.
### If you have a suggestion, please consider the cost and the availability of the parts. If you have a design change, please consider the ease of printing and the ease of assembly.
### If you have a request, please consider the goals of the project, and the limitations of the stock parts.

## TODO's and notes
    - Still working on the Z axis, it's not quite there yet
    - BOM needs completed, and to include different configurations
    - V-wheel X gantry design for stock print head and for afterburner
    - Need to optmize for printing without support
    - The wiring is a hot mess, there is no cable management or electronics mounting designed currently
    - Need to come up with an orgizational structure for different conversion types, (i.e. v-wheels vs linear rails, stock motors or upgraded etc.)

# Sources and mentions
The only reason this project was possible, and frankly, why I was able to create the first concept so quickly, is because of awesome open source projects! I don't want anyone to think that I did something amazing here, I simply adapted what I could from others, and made a few parts that weren't out there yet.

Of course [Voron Design](https://vorondesign.com/). An amazing, very generous engineering team.

[Marlin](https://github.com/MarlinFirmware/Marlin), Making the maker world a better place.

This wonderful person [Greg191134](https://github.com/Greg191134) is the source of the 5015 fan mod for the afterburner: [Afterburner 5015 fan mod](https://github.com/Greg191134/Voron/tree/master/Afterburner%20Optimisation/5015%20fan%20mod). They also have an awesome project called the Vorender-4, where they upcycled an ender 4 with an adaptation of the Trident gantry. 
