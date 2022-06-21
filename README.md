### latlon2cart
With this class you can convert geographical coordinates (Latitude, Longitude, Elevation)
to generic cartesian coordinates East, North, Up (in meters). In ordert to use it you first need to define
a reference point (Latref,Lonref,Eleref). All the calculations are performed using WGS84 ellipsoid.

## INSTALLATION:
from the terminal type:

sudo python3 setup.py install

## IMPORTANT: 
For Geographical Coordinates
Latitude is in degrees e.g. 36.117
Longitude is in degrees e.g. -117.854
Elevation is kilometers   
For E,N,U Cartesian Coordinates
East, North and Up are in meters

## USAGE:
You generate an object coordinates as:

import latlon2cart
    
region=latlon2cart.Coordinates(latref,lonref,eleref)
    
Then any other point (Lat_i, Lon_i, Ele_i) can be converted in the cartesian E,N,U frame as:

E_i,N_i,U_i = region.geo2cart(Lat_i,Lon_i,Ele_i)

To go back to the geographical coordinate system from the cartesian fram (E_i, N_i, U_i) you can use:

Lat_I,Lon_I, Ele_I=region.cart2geo(E_i,N_i,U_i)

## AUTHOR: 
Francesco Grigoli, 
Department of Earth Sciences, 
University of Pisa,
Italy
