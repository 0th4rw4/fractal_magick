Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

RECURSION


Creates a recursive affine composite effect in an image.

Download Script

last modified: August 27, 2013



USAGE: recursion [-d dist] [-z zoom ] [-a angle] [- r rot] [-i iter] infile outfile
USAGE: recursion [-h or -help]

-d ..... dist ..... distance to shift on each iteration;
................... float>=0; default=10
-z ..... zoom ..... zoom factor for each iteration;
................... 0<float<=1; default=.8
-a ..... angle .... angular direction to shift on each iteration;
................... -180<=float<180 degree; default=0
-r ..... rot ...... amount of rotation of image on each iteration;
................... -180<=float<180 degrees; default=0
-i ..... iter ..... number of iterations; integer>0; default=8
PURPOSE: To create a recursive affine composite effect in an image.

DESCRIPTION: RECURSION create a recursive affine composite effect in an image. The image is scaled, rotated and shifted by the specified amount on each iteration and then composited over the previous result.

ARGUMENTS:

-d dist ... DIST is distance to shift the image on each iterations. Values are floats >= 0. Typical values are between 10 and 20. The default=10.

-z zoom ... ZOOM is scale factor to apply to the image on each iteration. Values are 0

-a angle ... ANGLE is the direction angle to shift the image on each iteration. It is specified as a counterclockwise rotation -180<=float<=180 degrees. Typical values are between 0 and 90. The default is 0 (along the positive x direction).

-r rot ... ROT is the amount to rotate the image on each iteration. It is specified as a clockwise rotation -180<=float<=180 degrees. Typical values are betwen 0 and 30. The default is 0.

-i iter ... ITER is the number of iterations in the recursion. Typical values are between 5 and 20. Values are integers>0.

CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.


EXAMPLES


Recursion
http://www.jhlabs.com/ip/filters/

Original


Arguments:
-d 10 -a 0 -r 0 -z 0.8 -i 8

Arguments:
-d 10 -a 90 -r 0 -z 0.85 -i 8

Arguments:
-d 10 -a 45 -r 0 -z 0.85 -i 8

		
Arguments:
-d 15 -a 0 -r 45 -z 0.85 -i 8

Arguments:
-d 15 -a 45 -r 10 -z 0.85 -i 8

Arguments:
-d 20 -a 45 -r 20 -z 0.8 -i 10

		
More in: [http://www.fmwconcepts.com/imagemagick/recursion/index.php](http://www.fmwconcepts.com/imagemagick/recursion/index.php)