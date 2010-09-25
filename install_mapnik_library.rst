**********************
Install Mapnik Library
**********************

The Mapnik Library can be installed in several ways, choose only one
of:

- Install from your package manager
- Install from binaries
- Install stable Mapnik from source
- Install latest Mapnik from source
- tba

Is everything up to date on your system?

::

  sudo aptitude update
  sudo aptitude safe-upgrade


Install Mapnik Library from Package Manager
===========================================

This may not be the most recent version of Mapnik, depending on your
distribution.

::

  sudo aptitude install mapnik


Install Mapnik Library from Binaries
====================================

Windows and MacOSX binaries are available.  See installation
instructions for Windows and MacOSX.

  TODO: have build server create .deb, .rpm binaries

  TODO: add installtion instructions for MacOSX

  TODO: add installation instructions for Windows
  


Install Latest Stable Mapnik Library from Source
================================================

::

  
  cd ~/src
  svn co http://svn.mapnik.org/tags/release-0.7.1/ mapnik
  cd mapnik
  python scons/scons.py configure INPUT_PLUGINS=all OPTIMIZATION=3 SYSTEM_FONTS=/usr/share/fonts/truetype/
  python scons/scons.py
  sudo python scons/scons.py install
  sudo ldconfig

If Mapnik compiles without errors, confirm that python can find
Mapnik.

::  
 
  python
  >>> import mapnik
  # if python returns the 3-chevron prompt below without errors mapnik was properly detected
  >>> 



