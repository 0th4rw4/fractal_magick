Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

PIXELIZE


Creates a pixelized or blocky effect in an image.

Download Script

last modified: August 27, 2013



USAGE: pixelize [-s size] [-m mode] infile outfile
USAGE: pixelize [-h or -help]

-s .... size ..... pixelization size; size>0; default=3
-m .... mode ..... mode of minimizing; 1=resize; 2=sample; default=1

PURPOSE: To create a pixelized or blocky effect in an image.

DESCRIPTION: PIXELIZE creates a pixelized or blocky effect in an image where more pixelization (larger sizes) create larger blocky effects.

ARGUMENTS:

-s size ... SIZE is the pixelization (block) size. Values are greater than 0. The default is 3.

-m mode ... MODE is the mode of minimizing. Choices are 1 for -resize and 2 for -sample. The default=1

CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.


EXAMPLES


Image Pixelization
http://www.cescg.org/CESCG97/boros/

Original

Arguments:
-s 3

	
Arguments:
-s 5

Arguments:
-s 7

	
Arguments:
-s 9 -m 1

Arguments:
-s 9 -m 2

More in: [http://www.fmwconcepts.com/imagemagick/pixelize/index.php](http://www.fmwconcepts.com/imagemagick/pixelize/index.php)
