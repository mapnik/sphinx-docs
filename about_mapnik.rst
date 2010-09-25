
******
Mapnik
******

Mapnik is about making beautiful maps. It uses the `AGG library
<http://www.antigrain.com/>`_ or `Cairo library
<http://www.cairographics.org/>`_ and offers world class anti-aliasing
rendering with subpixel accuracy for geographic data. It is written
from scratch in modern C++ and doesn't suffer from design decisions
made a decade ago. When it comes to handling common software tasks
such as memory management, filesystem access, regular expressions,
parsing and so on, Mapnik doesn't re-invent the wheel, but utilizes
best of breed industry standard libraries from http://boost.org.



History
=======

Mapnik was started in a warm June afternoon in 2005 by Artem
Pavlenko. First version was released in ...

Current version is 0.7.1 available for download at
http://mapnik.org/download/.


Community
=========

Mapnik community is organized around main site http://mapnik.org and
development site http://trac.mapnik.org on which you can find latest
news about Mapnik and its development. Development site is organized
like a wiki which contains a lot of useful information, and you can
freely contribute if you `sign up <http://trac.mapnik.org/register>`_.

Also you can ask questions on mailing lists `mapnik-users
<http://lists.berlios.de/mailman/listinfo/mapnik-users>`_ and if you
want to help developing Mapnik check out `mapnik-devel
<http://lists.berlios.de/mailman/listinfo/mapnik-devel>`_. On this
links you will also find mailing list archive, which you should check
before asking your question. You can follow mailing lists on `Nabble
<http://old.nabble.com/Mapnik-f28006.html>`_.

If you like more direct communication you can find us on **#mapnik** at
irc.freenode.net, feel free to drop in with your question anytime.

Platforms
=========

Mapnik is a cross platform toolkit that runs on Windows, Mac, and
Linux (since release 0.4). Users commonly run Mapnik on Mac >=10.4.x
(both intel and PPC), as well as Debian/Ubuntu, Fedora, Centos,
OpenSuse, and FreeBSD. 

Supported data formats
======================

Mapnik uses a plugin architecture to read different
datasources. Current plugins which are considered stable, and built by
default, are:

* *shape* - support for accessing `ESRI Shape 
  <http://en.wikipedia.org/wiki/Shapefile>`_ files
* *postgis* - support for accessing geospatial data through `PostGIS
  <http://en.wikipedia.org/wiki/PostGIS>`_, the spatial database
  extension for `PostgreSQL
  <http://en.wikipedia.org/wiki/PostgreSQL>`_
* *raster* - stripped or tiled raster TIFF image dataset support 

Other plugins are not unstable but as they were added later in
development and there could still be some issues:

* *gdal* - support for `GDAL <http://www.gdal.org/formats_list.html>`_
  datasets
* *ogr* - support for `OGR
  <http://www.gdal.org/ogr/ogr_formats.html>`_ datasets
* *osm* - support reading `OpenStreetMap
  <http://www.openstreetmap.org>`_ XML dataset
* *sqlite* - support for `SQLite
  <http://en.wikipedia.org/wiki/SQLite>`_ / `Spatialite
  <http://www.gaia-gis.it/spatialite>`_ sql vector format
* *occi* - support for `oracle spatial
  <http://en.wikipedia.org/wiki/Oracle_Spatial>`_ 10g (versions
  10.2.0.x) sql vector format 
* *kismet* - support for `kismet <http://www.kismetwireless.net/>`_
  GPS support shows little WLAN nodes on the map
* *rasterlite* - support for `Rasterlite
  <http://www.gaia-gis.it/spatialite>`_ sqlite raster with wavelet
  compression

More data access plug-ins will be available in the future. If you
cannot wait and/or like coding in C++, why not write your own data
access plug-in?

Future
======

Large number of developers and contributors are actively developing
*mapnik2* which will become **0.8.0**. Also, version **0.7.2** is
scheduled to be released shortly.
