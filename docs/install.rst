
=========================
Installation instructions
=========================

The Short Version
-----------------

::

   make
   make py
   make extra
   make install  # to put it in /usr/local/astrometry
   # or:
   make install INSTALL_DIR=/some/other/place


If that worked, read no further!

Prerequisites
-------------

You will need:

  * GNU build tools (gcc/clang, make, etc.)
  * cairo
  * netpbm
  * libpng
  * libjpeg
  * libz
  * python (probably >= 2.4)
  * numpy
  * pyfits: http://www.stsci.edu/resources/software_hardware/pyfits
  * cfitsio: http://heasarc.gsfc.nasa.gov/fitsio/

Ubuntu / Debian
---------------

This should work::

    $ sudo apt-get install libcairo2-dev libnetpbm10-dev netpbm \
                           libpng12-dev libjpeg-dev python-numpy \
                           zlib-devel python-pyfits cfitsio-dev

RedHat / Fedora
---------------

Something like::

    $ sudo yum install cairo.x86_64 cairo-devel.x86_64 netpbm.x86_64 \
                       netpbm-devel.x86_64 fontconfig-devel.x86_64 \
                       libXrender-devel.x86_64 xorg-x11-proto-devel.x86_64 \
					   zlib-devel libjpeg-devel

I don't know what the *cfitsio* packages is called -- anyone?

Mac Homebrew
------------

These instructions *Worked For Me* as of September 2012 on OSX 10.8.

If you haven't already set up homebrew:
  * grab `XCode <https://developer.apple.com/xcode/>`_ (from the Apps Store.  Free, but you still need a credit card.  Argh.)
  * grab `XCode Command-line utilities <https://developer.apple.com/downloads/index.action>`_
  * grab `XQuartz <http://xquartz.macosforge.org/landing/>`_
  * grab `Homebrew <http://mxcl.github.com/homebrew/>`_
  * grab `pip <http://www.pip-installer.org/en/latest/installing.html>`_ if you don't have it already


Get homebrew dependencies that need special instructions::

    $ brew install --HEAD --use-gcc netpbm

Optionally, grab some other handy homebrew packages::

    $ brew install cfitsio --with-examples
    $ brew install md5sha1sum     # OSX doesn't come with this?!  For shame

Finally::

    $ brew tap camphogg/homebrew-science
    $ brew install astrometry.net

