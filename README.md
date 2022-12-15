Each row of the image is autolevelled.

This is useful for analysis of sprays videos.

Especially after background has been removed from the image, 
the downstream droplet cloud is rather diffuse, and low greyscale.
The initial liquid sheet is often quite well resolved.

It's much more useful for the user to be able see both initial sheet and later droplet cloud 
at about the same contrast ratio.

Also, if the spray nozzle hasn't been exactly static during the acquisition, because it is
opaque, it ias often at higher contrast than the spray: if you autolevel the whole spray 
image, the nozzle (uninteresting) is often better resolved than the spray.  If you do the 
re-levelling by row, it's only the first bits of the the liquid sheet (which are normally 
relatively easy to edge find) that are reduced contrast relative to the nozzle.

In all the spray numerical analysis routines I've written, 
the spray has been set to be topCentre-down (either as that was the experimental configuration 
(it normally is) or the image has been rotated that way for processing (just about the only 
exception are consumer spray bottles, or paint sprays, in field-trial orientation.  
Lab setups are almost always top down.

Hence, levelling each row of the image.

Based on Johannes Schindelin's plugin tutorial template for processing each pixel of either
GRAY8, GRAY16, GRAY32 or COLOR_RGB images.

And for COLOR_RGB, acknowledging Kieren Holland's RGB_Recolor as a useful exemplar of use of the ColorProcessor class


Public domain, copyright Prof Phil Threlfall-Holmes, TH Collaborative Innovation, 2022