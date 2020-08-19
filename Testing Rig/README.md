# Testing Rig

### Overview

The purpose of this testing rig is to measure force over a distance.
Note that this was done on a budget.  All of these parts can be purchased inexpensively, but appear to be giving good results so far.  As a result of the budget, there are some limitations.  The biggest one is that the sample rate is slow enough that good force measurements cannot be taken while the stepper motor is moving.  As a result, it can take a long time to perform a test run.

### Hardware

* Load cell
	* https://www.aliexpress.com/item/32860114708.html?spm=a2g0s.9042311.0.0.5fac4c4d4d88OH
	* The load cell I used came with the load cell converter board, however I wouldn't suggest using it.
* Load Cell Converter
	* The load cell converter board is an hx711.  There are multiple versions of this board.  The one included with the load cell I purchased generations a fair amount of noise.  I've filtered out most of the noise in my code, but not all of it.  I've read that there is a version of the hx711 that uses larger capicators that remove a lot of the noise, but I haven't tested with one yet.
* Stepper motor
	* https://www.amazon.com/gp/product/B01IP7IOGQ/ref=ppx_yo_dt_b_asin_title_o06_s00?ie=UTF8&psc=1
* Linear Rails
	* https://www.aliexpress.com/item/4000215698408.html?spm=a2g0s.9042311.0.0.5fac4c4d4d88OH
	* https://www.aliexpress.com/item/4000011179319.html?spm=a2g0s.9042311.0.0.5fac4c4d4d88OH
	* The bearings I purchased were pretty gritty.  I disassembled them and cleaned them, but I would suggest spending a little more money for something better.
* Lead Screw
	* https://www.mcmaster.com/98935A703/
	* https://www.mcmaster.com/94815A007/
	* I started out with a metric lead screw, but it was way too coarse of a pitch.  I wasn't able to find a good metric leadscrew that was in my budget, so this is what I ended up using.
* Calipers
	* https://www.amazon.com/gp/product/B085PWYSPK/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&psc=1
	* You'll need some additional electronical bits to get this to work.  See the forum post below under *Resources*
	* There are lots of cheap calipers that will work, most of which have a pcb that look like they're made in the same factory.  This was the second set I purchased.  The first set was from harbor freight, and they use a different board that I wasn't able to get to work.
	* These will need to be modified to fit this project.  The fixed jaw will need to be removed, and the board will need to be removed from the sliding jaw.
* Raspberry pi
	* I used an old B+ model, just about any pi should work, as long as you have enough GPIO pins.

### Software

Full disclosure, I'm not a python expert.  Some of this code was borrowed from people smarter than me (mostly the code used to get data from the calipers.  See the forum post below for details).  The caliper code runs on python 2.7, and is not compatible with python 3.  The rest of the code runs on python 3.  If someone wants to convert the caliper code over to python 3, feel free.

### Resources

The following resources were used while building this rig:

* https://tutorials-raspberrypi.com/digital-raspberry-pi-scale-weight-sensor-hx711/
* https://www.raspberrypi.org/forums/viewtopic.php?t=120513