Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

KMEANS


Applies k-means color reduction to an image.

Download Script

last modified: June 25, 2014



USAGE: kmeans [-n numcolors] [-s seedcolors] [-m maxiters] [-c convergence] [-C colorspace] [-v view] infile outfile
USAGE: kmeans [-h or -help]

-n ... numcolors ..... number of colors to use as seeds; integer>1; default=5
-s ... seedcolors .... list of seed colors rather than selecting a number of 
...................... colors; space separate list of opaque color; default 
...................... is to use the number of colors
-m ... maxiters ...... maximum number of iterations before stopping; 
...................... integer>0; default=40
-c ... convergence ... minimum rmse (times 100) between previous and current 
...................... set of colors to stop iterating; default=0.05
-C ... colorspace .... colorspace in which to do processing; default=sRGB
-v ... view .......... hexcolors (only), swatches (and hex colors), 
...................... progress (and hex colors), all

PURPOSE: To apply k-means color reduction to an image.

DESCRIPTION: KMEANS applies k-means color reduction to an image. This is a colorspace clustering or segmentation technique. The user must specify either a number of desired final colors or a set of initial seed colors. If a list of seed colors is not provided, then seed colors will be estimated using IM -colors (color quantization). The algorithm uses the seed colors to group (cluster) each pixel in the image according to the smallest rmse value to each seed color. Then it computes the new mean colors from the clusters. This process iterates until either the convergence value is reached or the maximum number of iterations is reached. The script is limited to fully opaque images.

Arguments:

-n numcolors ... NUMCOLORS is the number of colors to use as seeds. Values are integer>1. The default=5.

-s seedcolors ... SEEDCOLORS is a space delimited list of opaque seed colors. It is used rather than just selecting a given number of colors. Providing a well selected list of colors can make the iteration process quicker. Any valid set of opaque IM colors may be used. This includes rgb, hex or color names. However, there must not be any spaces in the color, especially for rgb color definitions. The default is to just use the desired number of colors.

-m maxiters ... MAXITERS is the maximum number of iterations before stopping. Values are integer>0. The default=40

-c convergence ... CONVERGENCES is the minimum rmse (times 100) between the previous and current set of colors to stop iterating. Values are floats>=0. The default=0.05

-C colorspace ... COLORSPACE in which to do processing; default=sRGB; other colorspaces that do well are YCbCr and LAB.

-v view ... VIEW permits one to list to the terminal or display any of the following options: hexcolors, swatches (and hex colors), progress (and hex colors), all. Hexcolors will list to the terminal the initial seed and final cluster colors in hex notation. Swatches will display the initial and final cluster colors as images to the display. It will also list the hex colors to the terminal. Progress will list each iteration and rmse value to the terminal in addition to the list of initial and final hex colors. All will do all of the above. The default none of the above. Note that hexcolors and swatches will be presented in the working colorspace and not converted to sRGB

References: http://en.wikipedia.org/wiki/Kmeans

NOTE: the script may be slow due to its iterative nature.

CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.


EXAMPLES

Example 1 -- Variation Number of Colors Vs Seed Colors 
( results should be identical )

Original Image
(source image)


Arguments:
-n 4

Arguments:
-s "blue green1 orange black"

	


Example 2 -- Variation in Colorspace

Original Image
(source image)


Arguments:
-n 5 -c sRGB

Arguments:
-n 5 -c YCbCr

Arguments:
-n 5 -c YIQ

Arguments:
-n 5 -c LAB

			


Example 3 -- Variation in Colorspace

Original Image


Arguments:
-n 5 -c sRGB

Arguments:
-n 5 -c YCbCr

Arguments:
-n 5 -c LAB

		
More In: [http://www.fmwconcepts.com/imagemagick/kmeans/index.php](http://www.fmwconcepts.com/imagemagick/kmeans/index.php)