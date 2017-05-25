# Leaflet.OS.Graticule
Add UK Ordinance Survey style 1km grid squares to your leaflet maps.

Demo: http://htmlpreview.github.io/?https://github.com/jonshutt/Leaflet.OS.Graticule/blob/master/demo.html

Usage
-----

```JavaScript

    var map = L.map('map',{
      center: [56.7969, -5.0036],
      zoom: 14,
    });

    L.tileLayer(
      'http://{s}.tile.opencyclemap.org/cycle/{z}/{x}/{y}.png', {
        maxZoom: 18,
      }
    ).addTo(map);

    var options = {      
    };

    L.osGraticule(options).addTo(map);

```

Notes
-----
This is UK based grid, it will continue to display outwith the lat/lng bounds of the UK however it will become more and more distorted until at some point it stops displaying.

Options
-------
- interval. Default = 1000. This draws a grid line every 1000m.
- showLabels: Default = true. Displays numeric Easting and Northings on the lines
- redraw: Default = 'move'. Sets when the grid is redrawn.
- maxZoom: Default = 15. Limit the range that the grid is drawn.
- minZoom: Default = 12. Limit the range that the grid is drawn.
- gridLetterStyle: Default = 'color: #216fff; font-size:12px;'. A css string to style the labels.


Code inspiration from https://github.com/ablakey/Leaflet.SimpleGraticule
