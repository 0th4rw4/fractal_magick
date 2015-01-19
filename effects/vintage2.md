Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

VINTAGE2


Applies a colorful vintage effect to an image.

Download Script

last modified: August 27, 2013



USAGE: vintage2 [-c1 color1] [-c2 color2] [-a coloramount] [-b brightness] [-c contrast] [-s vignetteshape] [-r vignetterounding] [-l vignettelighten] [-N noiseamount] [-L verticallines] [-B verticalbands] [-S backgroundmix] [-T bordertype] [-W borderwidth] [ -R borderrounding] [-C bordercolor] infile [backgroundfile] outfile 

USAGE: vintage2 [-h or -help]

-c1 .. color1 ............. color1 for vintage colorizing; default=yellow
-c2 .. color2 ............. color2 for vintage colorizing; default=green
-a ... coloramount ........ colorizing amount; 0<=integer<=100; default=15 
-b ... brightness ......... vintage brightness; -100<=integer<=100; 
........................... default=10
-c ... contrast ........... vintage contrast; -100<=integer<=100; 
........................... default=-20
-s ... vignetteshape ...... vignette shape; choices are: roundrectangle, 
........................... horizontal, vertical or none; 
........................... default=roundrectangle
-r ... vignetterounding ... vignette rounding percent for roundrectangle 
........................... only; 0<=integer<=50; default=50 for 
........................... roundrectangle and default=20 otherwise
-l ... vignettelighten .... vignette ligntening; 0<=integer<=100; default=0
-N ... noiseamount ........ noise amount; 0<=integer<=100; default=30 
-L ... verticallines ...... intensity of vertical lines; 0<=integer<=100; 
........................... default=25 
-B ... verticalbands ...... intensity of vertical bands; 0<=integer<=100; 
........................... default=30 
-M ... backgroundmix ...... background mixing; 0<=integer<=100;
........................... default=35
-T ... bordertype ......... border type; choices are: none, torn, rounded; 
........................... default=none
-W ... borderwidth ........ border width only for bordertype=torn; 
........................... integer>=0; default=5
-R ... borderrounding ..... border rounding percent only for 
........................... bordertype=rounded; 0<=integer<=50; default=10
-C ... bordercolor ........ border color; default=white

The backgroundfile is any texture image that is as large or larger than the image to be processed. Typically the backgroundfile should be converted to grayscale before using.

PURPOSE: To apply a colorful vintage effect to an image.

DESCRIPTION: VINTAGE2 applies a colorful vintage effect to an image. The vintage effect includes: two color choices, noise, lines, various vignette types and various border types.

ARGUMENTS:

-c1 color1 ... COLOR1 is the first color for vintage colorizing. Any valid IM color is allowed. The default=yellow.

-c2 color2 ... COLOR2 is the second color for vintage colorizing. Any valid IM color is allowed. The default=green.

-a coloramount ... COLORAMOUNT is the amount of vintage colorizing. Values are integers between 0 and 100. The default=15.

-b brightness ... BRIGHTNESS is the vintage brightness. Values are integers between -100 and 100. The default=10.

-c contrast ... CONTRAST is the vintage contrast. Values are integers between -100 and 100. The default=-20.

-s vignetteshape ... VIGNETTESHAPE is the vignette shape. Choices are: roundrectangle (r), horizontal (h), vertical (v) or none (n). The default=roundrectangle.

-r vignetterounding ... VIGNETTEROUNDING is the vignette rounding percent for the roundrectangle shape only. Values are integers between 0 and 50. The default=50.

-l vignettelighten ... VIGNETTELIGHTEN is the vignette ligntening. Values are integers between 0 and 100. The default=0.

-N noiseamt ... NOISEAMT is the amount of noise added. Values are integers between 0 and 100. The default=30.

-L verticallines ... VERTICALLINES is the intensity of vertical lines added. Values are integers between 0 and 100. The default=25.

-B verticalbands ... VERTICALBANDS is the intensity of vertical bands added. Values are integers between 0 and 100. The default=30.

-M backgroundmix ... BACKGROUNDMIX is the amount of background mixing with the image. Values are integers between 0 and 100. The default=35.

-T bordertype ... BORDERTYPE is the image border type. The choices are: none (n), torn (t) or rounded (r). The default=none.

-W borderwidth ... BORDERWIDTH is the image border width only for bordertype=torn and round. Values are integers between 0 and 100. The default=5.

-R borderrounding ... BORDERROUNDING is the image border rounding percent only for bordertype=rounded. Values are integers between 0 and 50. The default=10.

-C bordercolor ... BORDERCOLOR is the image border color. Any valid IM color is allowed. The default=white.

REFERENCES:
http://www.photoshop-plus.co.uk/2011/03/15/vintage-photo-effects-using-adobe-photoshop/
http://aceinfowayindia.com/blog/2009/12/how-to-create-vintage-photo-effect-photoshop-tutorial/
BACKGROUNDS:
http://www.flickr.com/photos/borealnz/sets/72157610307314214/with/3495540187/

http://www.flickr.com/photos/borealnz/3495540187/in/set-72157610307314214
http://www.flickr.com/photos/borealnz/3124030212/in/set-72157610307314214
http://lostandtaken.com/

http://www.unsigneddesign.com/LT_AntiquePaper.zip
http://www.unsigneddesign.com/LT_MicroscopicGrit.zip
CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.


EXAMPLES


Example 1 - Variation in Background
(source)

Original Image


Arguments:
grunge backgroundfile


Arguments:
oldpaper backgroundfile


Arguments:
weave backgroundfile


Arguments:
no backgroundfile




Example 2 - Variation in Border
(source)

Original Image


Arguments:
-T round
grunge backgroundfile


Arguments:
-T torn
grunge backgroundfile


Arguments:
-T none
grunge backgroundfile




Example 3 - Variation in Vignette Type
(source)

Original Image


Arguments:
-s roundrectangle
no backgroundfile


Arguments:
-s horizontal
no backgroundfile


Arguments:
-s vertical
no backgroundfile


Arguments:
-s none
no backgroundfile




Example 4 - Variation in Colors
(source)

Original Image


Arguments:
-c1 yellow -c2 green
grunge backgroundfile


Arguments:
-c1 green -c2 blue
grunge backgroundfile


Arguments:
-c1 yellow -c2 purple
grunge backgroundfile


More in: [http://www.fmwconcepts.com/imagemagick/vintage2/index.php](http://www.fmwconcepts.com/imagemagick/vintage2/index.php)