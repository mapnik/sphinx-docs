**************************************************
Load PostGIS Database with Initial Geographic Data
**************************************************

There are several ways to populate your geographic database.  Choose
only one of the following:

- OpenStreetMap "Planet" File
  
  The OpenStreetMap "Planet" file contains data for the entire planet.
  This is a large file and can stress computers ( and first-time users
  ).

- OpenStreetMap "Extract" File

  OpenStreetMap "Extract" files contain the OpenStreetMap data for a
  single region, usually a single country, state or province.  These
  are more managable than the "Planet" file while still often being
  substantial.

- OpenStreetMap API Bounding Box

  Smaller areas, sometimes town-sized, can be downloaded through the
  OpenStreetMap API.

- Postgresql dump file

  
OpenStreetMap Planet File
=========================

Aquire the complete OpenStreetMap database, also called the "planet
file" and load it in to the PostGIS database.

Aquire the Planet File
----------------------

A new "planet" file is published approximately each week. The mirror
and archives of the "planet" files are found at
http://planet.openstreetmap.org/ . In July 2010 the planet file was
about 10GB in length. If you are not interested in the entire planet
you can choose to download an extract file instead.

Install the Planet File
-----------------------

Using osm2pgsql or another tool.


OpenStreetMap Extract File
==========================

OpenStreetMap Extract files typically include a single country, state
or province.  They are published periodically by various sites
including

- http://download.geofabrik.de/osm/
- http://download.cloudmade.com/
- others

Aquire the Extract File
-----------------------







