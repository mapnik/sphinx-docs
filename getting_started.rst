***************
Getting Started
***************

After reading this document you should be able to create a simple
rendered map using Python or C++. 

TODO: add final rendered image


What do I need to get started?
==============================

First of all you need to install Mapnik library to your system. There
are to two basic ways to do it, you can either download binaries or
build library yourself from source. Installation from soruce if far more
complex and it documented in ..link to document...

Installation depends on your operating system and following sections
describe this process.

Windows installation
--------------------

Installing Mapnik on windows consists of following steps:

1. Install prerequisites
2. Download and unzip Mapnik binary
3. Set your system and/or users environment variables

Each of this steps is explained in detail ..here..!

Linux installation
------------------

Most modern Linux distributions include Mapnik binaries in their
repositories. Installation method depends your distribution:

* Debian or Ubuntu ::

  # aptitude install python-mapnik

* Fedora ::

  # yum install mapnik-python

* Archlinux ::
  
  # pacman -S mapnik

MacOSX installation
-------------------

Dane Springmeyer kindly hosts and builds MacOSX Mapnik binaries, you
can find more information on his download page
http://dbsgeo.com/downloads/.

Testing Mapnik installation
===========================

Easiest way to test if you have successfully installed and configured
Mapnik is to start up your Python interpreter and try to import mapnik
library: ::

   $ python
   Python 2.6.5 (r265:79063, Apr  1 2010, 05:28:39) 
   [GCC 4.4.3 20100316 (prerelease)] on linux2
   Type "help", "copyright", "credits" or "license" for more information.
   >>> import mapnik
   >>>

If there are no errors or complaints, you're on the right track. You
can also try to find out which Mapnik version are you currently
running by executing following code: ::

   >>> import mapnik
   >>> mapnik.mapnik_version()
   701
   >>>

That's it you are ready to create your first map using Python
scripting language.
