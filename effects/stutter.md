Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

STUTTER


Creates a 'stuttered' offset-like effect in an image.

Download Script

last modified: August 27, 2013



USAGE: stutter [-s size] [-d direction] infile outfile
USAGE: stutter [-h or -help]

-s .... size ......... stutter offset size; size>0; default=16
-d .... direction .... x,h,horizontal or y,v,vertical or xy,vh,both;
...................... default=x

PURPOSE: To create a "stuttered" offset-like effect in an image.

DESCRIPTION: STUTTER creates a "stuttered" offset-like effect in an image.

ARGUMENTS:

-s size ... SIZE is the stutter offset size. Values are greater than 0. The default is 16.

-d direction ... DIRECTION is the stutter offset direction. Values may be horizontal specified as either x, h or horizontal; vertical specified as y, v or vertical or both specified as xy, hv or both. The default=x.

CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.


EXAMPLES


Image Stutter
http://www.cescg.org/CESCG97/boros/

Original


Arguments:
-s 16 -d x

Arguments:
-s 32 -d x

	
Arguments:
-s 16 -d y

Arguments:
-s 32 -d y

	
Arguments:
-s 16 -d xy

Arguments:
-s 32 -d xy

	
More In: [http://www.fmwconcepts.com/imagemagick/stutter/index.php](http://www.fmwconcepts.com/imagemagick/stutter/index.php)