# cnc

We're using this to keep track of using our CNC projects and protocols. I'm an amateur figuring out this by looking at resources online, so these are mostly just notes so I don't forget, but maybe others will find them useful, too.

## Machine itself

CNC: Purchased a [MySweety 3018](https://www.amazon.com/gp/product/B07DXMFY38/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) ("Upgrade Version CNC 3018 Pro GRBL Control DIY Mini CNC Machine, 3 Axis Pcb Milling Machine, Wood Router Engraver with Offline Controller, with ER11 and 5mm Extension Rod"). $269

**Pros:**

* Not too expensive
* Fairly large bed (3018 = 30 cm x 18 cm, not a model number)
* The offline controller doesn't require you to have a computer hooked up, can just use an SD card

**Cons:**

* Came with metal shavings and oil on all the aluminum beams, requiring a fair bit of cleaning
* The bolts connecting the bed to the sliding plastic were too short. Got some longer ones at Lowes; would have been better to order exactly the ones I wanted online, as these were a bit too long (used washers to fix this)
* Connection between the motors and threaded rods uses adaptors with set screws; so far, those have come loose about 2/3 of the time printing, making the print fail (b/c an axis of movement stops)

Overall, I think this was ok value for the price; had I more money available for this, I'd probably look into other options, though.

## Generating files

Like most CNC, uses g-code files (which have file extension .nc). Using http://easel.inventables.com has been good for generating these files. Exporting g-code requires a pro version, which is free four days a week (yay) but $20/month after that (we've gotten by with the free trials so far).

Some settings required to make it work for our machine:

* Machine -> Spindle control -> **Automatic**
* Machine -> RPM -> **12000**

Setting both of these are required for the spindle (the motor that turns the bit) to actually spin on our machine.

Bit: the bit that came with our machine was a 20 degree bit, 0.125 inches diameter. So need to set this as a custom V Bits in the bits menu.

To generate the gcode, Machine -> Advanced -> Generate g-code. Then a green Export g-code button will appear.

## Files

Files we've run (and are in the data dir)

**Burgoyne.nc** First output. My son wanted to do carving of John Burgoyne for a school project; the symbol on the right was for a birthday present. The head carving came out ok, the y axis failed on the design (collar between a motor and threaded rod came undone), and, oddly, the "e" was dropped off his last name in the final carving.

![Burgoyne in Easel](Burgoyne.jpg)

**Birthday.nc** Another try of the birthday design.
