Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

THERMOGRAPHY


Simulates a picture taken with a thermal imaging camera.

Download Script

last modified: August 27, 2013



USAGE: thermography [-l lowpt] [-h highpt] infile outfile
USAGE: thermography [-help]

-l ... lowpt .... low point value on color table; float; 0<=integer<=100; 
................. default=0
-h ... highpt ... hight point value on color table; float; 0<=integer<=100; 
................. default=100

PURPOSE: To simulate a picture taken with a thermal imaging camera.

DESCRIPTION: THERMOGRAPHY simulates a picture taken with a thermal imaging camera. The low point and high point can be used to shift and scale the color spectrum table.

ARGUMENTS:

-l lowpt ... LOWPT is the low point on the color table (violet end) to use to stretch and/or scale the color spectrum used. Values are integers between 0 and 100. The default=0 (full violet).

-h highpt ... HIGHPT is the high point on the color table (red end) to use to stretch and/or scale the color spectrum used. Values are integers between 0 and 100. The default=100 (full red).

CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.


EXAMPLES


Example 1

Original


Arguments:
-l 0 -h 100

Arguments:
-l 0 -h 50

Arguments:
-l 50 -h 100

		


Example 2

Original

Arguments:
-l 0 -h 100

	
More In: [http://www.fmwconcepts.com/imagemagick/thermography/index.php](http://www.fmwconcepts.com/imagemagick/thermography/index.php)