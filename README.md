Bsed off the jpeg-9a encoding library.

The changes to the JPEG library are a little rough. To use it, you'll need to
change some lines in jccoefct.c. Lines 209 and 223 are the parts that will
determine if the public part or the secret part are output. Change rfm_coef to
whatever coefficient you want and recompile.

Run with something like:
cjpeg -quality 100 -grayscale -outfile boat.512.jpeg boat.512.pnm 
