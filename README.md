MPL3115A2 Pressure Sensor library with calibration functions
==================

This library is a modified and extended version of the original at https://github.com/sparkfun/MPL3115A2_Breakout/

List of improvements / changes
------------------

Sensor calibration functions added by https://github.com/mariocannistra
Note: I've put together this code to obtain more precise values and a stable behavior from the sensor when using it both for altitude and pressure measurements

List of code merges and improvements:
- slightly customized the code by http://www.henrylahr.com/?p=99
- used the offset routines by Michael Lange (see https://developer.mbed.org/users/sophtware/code/MPL3115A2/ )
- completed with elevation_offset calculation by digitalmisery comment at https://www.sparkfun.com/products/11084
- then packaged the calibration function within the original 
library code by Nathan Seidle - SparkFun Electronics
- merged with latest Sparkfun fixes by https://github.com/ToniCorinne
- added some () in a couple of IFs per compiler warnings/suggestions
- added the proper register config calls sequences using setModeStandby() and setModeActive()
- fixed the pressure reading routine using the correct bit mask for PDR flag. Thanks to @lectroidmarc and @rabelux for listing the issue here: https://github.com/sparkfun/MPL3115A2_Breakout/issues/12  The chip datasheet https://cdn-shop.adafruit.com/datasheets/1893_datasheet.pdf at page 20 actually shows PDR as 0x04

New example for calibration usage
------------------
[*I added barometer_calibration.ino in the examples folder*](https://github.com/mariocannistra/MPL3115A2/blob/master/examples/barometer_calibration/barometer_calibration.ino)

It shows proper usage of the calibration functions.

Tested on Teensy 3.1 and Arduino Pro Micro.

License
------------------

Please see below and refer to the original sources for the license stuff. I guess it's all public domain but please check. And if you meet with Nathan for a beer let me know and consider as beerware my code as well.

Original library:
by Nathan Seidle
SparkFun Electronics
Date: September 22nd, 2013
License: This code is public domain but you buy me a beer if you use this and we meet someday (Beerware license).
