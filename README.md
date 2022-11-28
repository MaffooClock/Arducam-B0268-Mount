# Arducam B0268 16MP/105° USB Camera Mount

This is a minimalistic enclosure and mounting solution that I designed to mount my [Arducam B0268](https://www.arducam.com/product/arducam-16mp-wide-angle-usb-camera-for-laptop-1-2-8-cmos-imx298-mini-uvc-b0268/)[^1] for my Voron 2.4, although it could very likely fit a variety of other printer frames.

This camera is perfect for large printers like the 350mm² Voron 2, as the 105° viewing angle allows full view of the entire print bed for even the tallest print jobs without the "fisheye" distortion.

| ![Arducam B0268](/images/Arducam-B0268.png) | ![Animation of all components](/images/animation.gif) |
:---:|:---:

One of the components is actually from [C270 Mount](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Fiction/C270_mount) by Fiction#5826.

For the Voron 2, it's designed to mount on the underside of the top extrusion, with plenty of clearance between the doors and top panel, and it won't get in the way of any of the popular LED lighting mods (such as [this one](https://www.printables.com/model/84735-led-strip-holder-for-voron-24) by [FunFunBoy](https://www.printables.com/social/175028-funfunboy/about)).

[^1]: There is [a version of this camera](https://www.arducam.com/product/arducam-imx298-usb-camera-with-case-b026801/) that comes in a metal case, but I'm not sure how easy it would be to install on an enclosed Voron 2 without it bumping into the doors or top panel — maybe it works fine, I don't know.

## BOM

![Photo of all parts](/images/photo_parts.jpeg)

| Qty | Item                              |
|-----|-----------------------------------|
|   4 | M2x8 SHCS                         |
|   1 | M3 Heat-set Insert (5mm OD x 4mm) |
|   1 | M3x8 FHCS                         |
|   1 | M3x50 SHCS                        |
|   2 | M3 Washer                         |
|   1 | M3 Hex Nut                        |
|   2 | M3x6 SHCS                         |
|   2 | M3 T-Nut                          |


## Print Settings

The settings below are what I use by default, and are what worked with this design.  You're free to deviate as you see fit, if you know what you're doing.

| Setting           | Value       |
|-------------------|-------------|
| Material          | ABS         |
| Infill            | 40%, Gyroid |
| Layer Height      | 0.2mm       |
| Extrusion Width   | 0.4mm       |
| Wall Count        | 4           |
| Top/Bottom Layers | 4           |
| Supports          | Off         |

:warning: **Important considerations**:
- Make sure extruder flow is dialed in well — the tolerances are somewhat slim for most parts, so if your printer over- or under-extrudes, assembly might be challenging or suboptimal in some places.  The clamping mechanism is particularly tight (for obvious reasons).
- Make sure the bridging ability of your printer is decently tuned, as the rear cover has a 1mm inset that is printed with bridging; crappy bridging is almost certain to ruin this.  You can turn on supports for this area, but be sure to carve all of it out cleanly to ensure the rear stud can be attached straight and flat without causing a crooked image on the camera.


### Slicer Layout

I'm not smart enough to figure out how to export STLs from Fusion 360 in a way that will make them lay flat in your slicer the way they're supposed to, so you might have to handle this yourself.

![Screenshot of a slicer print bed](/images/print_bed.png)

The arrangement isn't important, just the orientation to the Z plane.


## Assembly

### Step 1

Make sure to insert the heat-set nut all the way into the lower cavity so that the top of the insert is flush with the inside rim — there should be a 1mm gap between the outer surface and the top of the heat-set insert.

Also, make sure to clean up any "elephant foot" or rough edges.

![Photo of heat-set insert in rear mounting stud](/images/photo_rear_stud.jpeg)

### Step 2

The rear cover has a 1mm inset area that the mounting stud will mate to.  Since this area uses a lot of bridging, you may have to perform some cleanup.

![Cleaning up the inset of the rear case for the mounting stud](/images/photo_rear_cover_cleanup.jpeg)

### Step 3

You may now attach the rear mounting stud to the rear case using the **M3x8 FHCS**.

![Photo of the rear cover with mounting stud attached](/images/photo_rear_assembled.jpeg)

### Step 4

Place the camera module into the front case upside-down, with the USB header on top and the heatsink on bottom.

![Photo of the front case with camera module inserted](/images/photo_front_assembled.jpeg)

Secure the rear cover assembly to the front case using the four **M2x8 SHCS** screws.

:point_right: _The screw holes inside the front case might be a little tight, so you may need to use an awl or 2mm drill bit to widen them out some._

### Step 5

Attach the mounting arm to the rear stud using the **M3x50** screw and **M3 hex nut**, with each of the **M3 washers** on each end of the screw.  Hand-tighten the nut for now, we'll tighten it completely after installation.

:point_right: _The washers are important for allowing you to tighten the clamp smoothly without gouging into the plastic._

![Photo of the completed assembly](/images/photo_assembled.jpeg)

### Step 6

Attach the USB cable to the header, then mount the completed assembly to the underside of the top extrusion using the two **M3 T-nuts** and **M3x6 SHCS** screws

| ![Photo of the assembly being mounted to printer frame](/images/photo_wired.jpeg) | ![Photo of the finished installation](/images/photo_mounted.jpeg) |
|:---:|:---:|

### Finish

Adjust the angle of the camera as you see fit.  For a 350mm² Voron 2, I recommend that the front edge of the build plate is just barely outside the bottom of the image, that way you get as much view area as possible for taller builds, as anything beyond the front edge of the build plate is just wasted.

![Snapshot from the installed assembly](/images/snapshot.jpeg)


## Contributing

Contributions and feedback are welcome, however, I don't intend for this to be an ongoing project.  The design meets my needs as-is, and I'm just sharing this for anyone else who might need it, therefore I am unlikely to tinker with it myself any further.

That said, _significant_ improvements that are likely to benefit current and future users of this solution will be sincerely considered as personal time permits.
