metromanila_malls
=======================

This script scrapes data about shopping malls in Metro Manila, Philippines from Wikipedia, excluding those under construction. It categorizes malls based on their developer and whether they are major developers.

Dependencies
------------
- requests
- BeautifulSoup
- re

Usage
-----
metromanila_malls.ipynb

Functions
---------
- `get_coordinates(place_name)`: Extracts mall data from a given table.
- `format_polygon_points(polygon_points)`: Formats polygon points as a string in the required format.
- `get_polygon_points(place_name)`: Retrieves polygon points from OpenStreetMap using an **API request** within the Philippines boundary.
------------------------------------------------------------------------------------------------------------

metromanila_malls_alt
=========================

This script reads the csv data produced by `metromanila_malls.ipynb` and fills in empty polygons. It is used when there is an issue with specific `mall_names`.

Dependencies
------------
- requests
- BeautifulSoup
- re
- pandas
- numpy
- osmnx
- geopandas

Usage
-----
metromanila_malls_alt.ipynb

Functions
---------
- `format_polygon_points(polygon_points)` and `format_polygon_points2(polygon_points)`: Formats polygon points as a string in the required format.
- `get_polygon_points(place_name)`: Retrieves polygon points from OpenStreetMap using an **API request** within the Philippines boundary.
- `get_polygon_points2(place_name)`: Retrieves polygon points **directly** from OpenStreetMap within the Philippines boundary.