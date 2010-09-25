************************
Install PostGIS Database
************************

Install Postgresql and PostGIS
==============================

Is everything up to date on your system?  

::

  sudo aptitude update
  sudo aptitude safe-upgrade

Install Postgresql and the PostGIS extensions to enable geographical
queries.

::

  sudo aptitude install postgresql-8.4-postgis postgresql-contrib-8.4
  sudo aptitude install postgresql-server-dev-8.4 
  sudo aptitude install build-essential libxml2-dev 
  sudo aptitude install libgeos-dev libpq-dev libbz2-dev proj
 
Configure the Postgresql Server
===============================

Edit the configuration file at
/etc/postgresql/8.4/main/postgresql.conf to set some resonable
defaults.  These changes help when dealing with large quantities of
data that are found in geographic some databases.

These edits are found in four places in the configuration file. 

::

  shared_buffers = 128MB # 16384 for 8.1 and earlier
  checkpoint_segments = 20
  maintenance_work_mem = 256MB # 256000 for 8.1 and earlier
  autovacuum = off

Configure runtime kernel parameters
===================================

Edit /etc/sysctl.conf to set kernel parameters after a restart.  

::

  kernel.shmmax=268435456 

Then apply the same kernel parameter now, without restarting.

::

  sudo sysctl kernel.shmmax=268435456

Restart the Postgresql Server
=============================

Restart the postgresql database server to enable the configuration
changes.

::

  sudo /etc/init.d/postgresql-8.4 restart  

The database server should restart without errors or warnings

   |  * Restarting PostgreSQL 8.4 database server
   |    ...done.

Create the Postgresql Database
==============================

Create a database called "gis". Some of our future tools presume that
you will use this database name. Substitute your username for
"username" in two places below. This should be the username that will
render maps with mapnik.

:: 

  sudo -u postgres -i
  createuser username # answer yes for superuser
  createdb -E UTF8 -O username gis
  createlang plpgsql gis
  exit

Apply the PostGIS Extensions to the Database
============================================

Apply the PostGIS extensions to the postgresql database.

::

  psql -f /usr/share/postgresql/8.4/contrib/postgis.sql -d gis

This should respond with many lines ending with

   |  ...
   |  CREATE FUNCTION
   |  COMMIT

Substitute your username for "username" in two places in the next
line. This should be the username that will render maps with mapnik.

::

  echo "ALTER TABLE geometry_columns OWNER TO username; ALTER TABLE
  spatial_ref_sys OWNER TO username;" | psql -d gis

Should reply with

   |  ALTER TABLE
   |  ALTER TABLE

Enable OpenStreetMap Updates
============================

This optional step is only required if you plan to use the
OpenStreetMap regular data updates.  Enable intarray to enable updates
through the OpenStreetMap .osc files for daily, hourly and minutely
updates.

::

  psql -f /usr/share/postgresql/8.4/contrib/_int.sql -d gis

Replies with many lines ending with

   |  ...
   |  CREATE FUNCTION
   |  CREATE OPERATOR CLASS

Set SRID for PostGIS Database
=============================

Set the Spatial Reference Identifier (SRID) on the new database.

::

  psql -f ~/bin/osm2pgsql/900913.sql -d gis

Should reply with

   |  INSERT 0 1










