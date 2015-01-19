Licensing:
Copyright © Fred Weinhaus

My scripts are available free of charge for non-commercial use, ONLY.

For use of my scripts in commercial (for-profit) environments or non-free applications, please contact me (Fred Weinhaus) for licensing arrangements. My email address is fmw at alink dot net.

If you: 1) redistribute, 2) incorporate any of these scripts into other free applications or 3) reprogram them in another scripting language, then you must contact me for permission, especially if the result might be used in a commercial or for-profit environment.

Usage, whether stated or not in the script, is restricted to the above licensing arrangements. It is also subject, in a subordinate manner, to the ImageMagick license, which can be found at: http://www.imagemagick.org/script/license.php

KALEIDOSCOPIC


Applies a kaleidoscope effect to an image.

Download Script

last modified: August 27, 2013



USAGE: kaleidoscopic [-m mode] [-o orient] [-i] [-s spread] [-d density] 
[-c curviness] [-D dimension] [-b blur] [-e emboss] [-S sharpen] 
[-B blend] [-n newseed] [-R] [infile] outfile

USAGE: kaleidoscopic [-h or -help]
-m .... mode ......... mode of effect; choices are: image, disperse 
...................... and random; default=image
-o .... orient ....... orientation of quadrant; choices are: 0, 90, 180
...................... and 270; default=0
-i ................... invert quadrant mask
-s .... spread ....... spread distance with mode=disperse; integer>0; 
...................... default=5
-d .... density ...... density or frequency mode=disperse; integer>0; 
...................... default=5
-c .... curviness .... curviness/clumpiness of dispersion; integer>=0; 
...................... default=10
-D .... dimension .... dimension of random noise image when no input image
...................... is provided; dimension is used for both width 
...................... and height; integer>0; default=128
-b .... blur ......... amount of blur to use with mode=random; integer>0
...................... default=5
-e .... emboss ....... amount of emboss effect with mode=random;
...................... integer>0; default=2
-S .... sharpen ...... amount of sharpening with mode=random; integer>=0
...................... default=0
-B .... blend ........ percent blend of random noise with image; 
...................... 0<=integer<=100; default=100 (all random noise)
-n .... newseed ...... new seed value; integer>0; default will randomly 
...................... change seed value for modes=random and disperse
-R ................... resize to minimum dimension of original image

If the input image is not square, the center square section will be used to
generate the kaleidoscopic effect.

If no input image is provided, a random noise image will be created of size determined from the provided dimension.
PURPOSE: To apply a kaleidoscope effect to an image.

DESCRIPTION: KALEIDOSCOPIC applies a kaleidoscope effect to an image. The image is transposed and composited with the original using a diagonal mask. This forms one quadrant. The other quadrants are 90, 180 and 270 rotations. The four created quadrants are then appended together to create the output. Optionally a dispersion effect may be applied to the image or the image may be mixed with random noise. If no input image is provided, the user may specify a size and a random image will be generated as the base image. The output will be twice the size of the cropped input image.

ARGUMENTS:

-m mode ... MODE of kaleidoscopic effect. The choices are: image (i), disperse (d) or random (r). The dispersion effect is applied to the image. The random effect may be appied to an input image which covers the image or a user supplied dimension may be provided to create a new image if no input image is supplied. Either way, the result will be the same.

-o orient ... ORIENT is the rotational oriention of the created image quadrant.

-i ... INVERT the mask so as to swap the input image and its transpose.

-s spread ... SPREAD distance with mode=disperse. Values are integers>0. Typical values range from 2 to 20. The default=5

-d density ... DENSITY is the closeness or frequency of detail with mode=disperse. Values are integers>0. The default=5.

-c curviness ... CURVINESS/CLUMPINESS with mode=disperse. Values are integers>=0. Small values produce fine, dust-like detail. Larger values produce more clumpy and curvy clusters. Typical values range from 0 to 20. The default=10

-D dimension ... DIMENSION will be the width and height of the random noise image when no input image is provided. Values are integers>0. One value is supplied and it will be used for both the width and height.

-b blur ... Amount of blur to use with mode=random. Values are integers>0; The default=5

-e emboss ... Amount of emboss to use with mode=random. Values are integers>0; The default=2

-S sharpen ... Amount of sharpening to use with mode=random. Value are integers>=0. The default=0

-B blend ... BLEND percent of random noise with the image. Values are integers between 0 and 100. The default=100 (all random noise).

-n newseed ... NEWSEED is the seed value to use for randomization. This permits the pattern to be repeated. The default is to change the seed value randomly each time the script is run, thus causing somewhat different patterns each time the script is run. This argument is used for both mode=random and mode=disperse.

-R ... RESIZE to minimum dimension of original image.

REQUIREMENT: IM 6.4.8.5 or higher due to the use of -evaluate sine and cosine

CAVEAT: No guarantee that this script will work on all platforms, nor that trapping of inconsistent parameters is complete and foolproof. Use At Your Own Risk.

EXAMPLES

Arguments:
-m image -o 0

Arguments:
-m image -o 90

Arguments:
-m image -o 180

Arguments:
-m image -o 270

Arguments:
-m image -o 0 -i

Arguments:
-m image -o 90 -i

Arguments:
-m image -o 180 -i

Arguments:
-m image -o 270 -i

More in: [http://www.fmwconcepts.com/imagemagick/kaleidoscopic/index.php](http://www.fmwconcepts.com/imagemagick/kaleidoscopic/index.php)