# Map-Generator

Generate a Google Map with your own markers, legend, and list of addresses!

# Setup

Open ***marker_updater.xlsm*** and Enable Contents. Specify one address per line with your InfoWindow Content, Full Address, [Latitude, Longitude], and Marker Color in columns A-D.

You may need to use a geocoding service such as [geocodio](https://www.geocod.io/) or [ESRI](https://www.esri.com/en-us/home) to get the latitude and longitude associated with each address. 

Column E contains the corresponding line in JSON for our marker that will be written to an external file. Drag the formulas in column E down so there is a line of JSON output for each marker.

Click the Update Map Markers button in the upper right. This runs a macro that will write JSON to each corresponding color-named JSON file in the ***./js/*** directory.

## Change the marker image(s) (optional)

Go to the ***./markers/*** directory and replace the color-named .png file with the .png image of your choice.

## Set up the map

Open ***map.html*** in a text editor. Replace "YOUR_KEY_HERE" on line 19 with your Google Maps Javascript API key.
Map controls are set in the JavaScript initialize() function starting on line 42. You can configure map controls, default zoom level and location, and map styles here. 
Change your map legend labels starting on line 107.

> **ProTip:** Please review the Google Maps JavaScript API documentation here: https://developers.google.com/maps/documentation/javascript/maptypes

## View the map

Open ***map.html*** in your browser.
