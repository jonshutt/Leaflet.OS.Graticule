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
- interval: 1000
- showLabels: true
- redraw: 'move'
- maxZoom: 15
- minZoom: 12
- gridLetterStyle: 'color: #216fff; font-size:12px;'



Code inspiration from  
