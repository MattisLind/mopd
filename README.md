mopd
====

mopd-linux-20000808

 This is the Linux version of Mats Janssons' Mopd.
 
 The sources here are taken from the NetBSD version of mopd 2.5.3/4 
 in CVS, plus some bits from the OpenBSD port, and the security 
 fixes reported on BUGTRAQ on 08 Aug 2000. 
 
 I had to rewrite the Makefiles, and hack things about a bit to compile 
 under Linux, So if this version doesnt work for you, send email to the 
 Linux/VAX list detailing the problem. 
 
 The mopa.out program does not work. The a.out structures have different
 names under NetBSD and Linux (see /usr/include/a.out.h), and so the 
 code needs re-writing.
 
 atp@pergamentum.com 8/Aug/2000
 
 Patches from John Nall added for Alpha/Linux
 

 2022-06-13

 Small change to make it compile on Linux kernel 5 with GCC 10.

 Tested working to download firmware to DECserver 100 terminal server.
 
 Added instructions on how to setup a DECserver 100.


Cloned from http://linux-vax.sourceforge.net/download/mopd-linux.tar.gz

Version at http://www.stacken.kth.se/~moj/mopd.html is currently inaccessible.
