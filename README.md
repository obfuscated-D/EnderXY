# Ender XY
This isn't a finished product / refined design. This was a *very* quick concept build (we're talking < 8hrs quick), and could absolutely use improvement. I hope it can serve as a decent starting point.

# What to expect
This is a pretty fun build, and in the end you do have a working, capable printer. However, 
keep in mind that this is made almost entirely from a *very cheap printer*. With no upgrades to the motors,extruder, or a linear rail conversion, it's not going to be a rapid, production level machine like a Bambu or a Voron.  

## Specs
Build volume (X,Y,Z):

V-wheel version | Linear rail version
--------------- | ------------------
200,185,185    | 200,200,185

## Design
The overall idea was to turn a cheap ender 3 into a good platform for a high performance core xy machine, incorporatating as many stock components as possible, to reduce the BOM.

You can use all the bone stock components and a very small list of extra materials, and make a functional corexy that prints faster than a stock ender 3. This allows easy incremental upgrades such as changing to direct drive extruders, larger stepper motors etc.

The design here pulls HEAVILY from [Voron Design](https://vorondesign.com/) components.

### The Gantry
The gantry is essentially a modified Trident gantry, and there are two versions in here, there is the v-wheel version, and the linear rail version. Of course, the linear rail version is better, but the V wheel version only needs some bolts and some printed parts, and it works fine. If you build the v wheel version, you can easily change over to the linear rail version in the future without any modification to the frame or belts. Just attach the rails and swap out the X beam ends. 

The V wheel version does limit the Y axis to 185mm, with the linear rail version you can get the full 200. 

### The Tool Head
I went with an Afterburner Bowden setup, The files in here allow you to use the stock ender3 hotend in the afterburner, and a 5015 blower fan.

Bowden feed is not the greatest, and is a limiting factor as far as print quality and speed are concerned. Direct drive would be much much better. Again, you can always upgrade to a stealthburner in the future!