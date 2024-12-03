# Ender XY
This isn't a finished product / refined design. This was a *very* quick concept build (we're talking < 8hrs quick), and could absolutely use improvement. I hope it can serve as a decent starting point.

# What to expect
This is a pretty fun build, and in the end you do have a working, capable printer. However, 
keep in mind that this is made entirely from a *very cheap printer*. With no upgrades to the motors,extruder, or a linear rail conversion, it's not going to be a rapid, production level machine like a Bambu or a Voron. This is more so a project for the love of the build. 

## Specs
Build volume (X,Y,Z):

V-wheel version | Linear rail version
--------------- | ------------------
200,185,185    | 200,200,185

## Cost
This will vary wildly with person and location. It's reasonable to assume you can get all the necessary parts for the basic stock conversion (not including the printer), for about $50usd. You'll probably use most of a 1kg spool of filament as well.

## Design
The overall idea was to turn a cheap ender 3 into a good platform for an easily upgradeable, affordable, core xy machine, incorporatating as many stock components as possible to reduce the BOM.

You can use all the bone stock components and a very small list of extra materials, and make a functional corexy that prints faster than a stock ender 3. This allows easy incremental upgrades such as changing to direct drive extruders, larger stepper motors etc.

The design here pulls HEAVILY from [Voron Design](https://vorondesign.com/) components.

### The Gantry
The gantry is essentially a modified Trident gantry, and there are two versions in here, there is the v-wheel version, and the linear rail version. Of course, the linear rail version is better, but the V wheel version only needs some bolts and some printed parts, and it works fine. If you build the v wheel version, you can easily change over to the linear rail version in the future without any modification to the frame or belts. Just attach the rails and swap out the X beam ends. 

The V wheel version does limit the Y axis to 185mm, with the linear rail version you can get the full 200. 

### The Tool Head
I went with an Afterburner Bowden setup, The files in here allow you to use the stock ender3 hotend in the afterburner, and a 5015 blower fan.

Bowden feed is not the greatest, and is a limiting factor as far as print quality and speed are concerned. Direct drive would be much much better. Again, you can always upgrade to a stealthburner in the future!

## Firmware
There is a ready to go firmware.bin in the firmware folder for the stock build on the creality 4.2.2 main board with A4988 stepper drives. You need to identify your board. If it is not the 4.2.2 with A4988 drivers, you will need to build a marlin image for your board. The configuration files needed for marlin 2.x are in the Marlin_files directory. See [Marlin](https://github.com/MarlinFirmware/Marlin) for more information on how to build your own firmware.


# Sources and mentions
The only reason this project was possible, and frankly, why I was able to create the first concept so quickly, is because of awesome open source projects! I don't want anyone to think that I did something amazing here, I simply adapted what I could from others, and made a few parts that weren't out there yet.

Of course [Voron Design](https://vorondesign.com/). An amazing, very generous engineering team.

This wonderful person [Greg191134](https://github.com/Greg191134) is the source of the 5015 fan mod for the afterburner: [Afterburner 5015 fan mod](https://github.com/Greg191134/Voron/tree/master/Afterburner%20Optimisation/5015%20fan%20mod). They also have an awesome project called the Vorender-4, where they upcycled an ender 4 with an adaptation of the Trident gantry. 