# Leaflet.OS.Graticule
Add UK Ordinance Survey style 1km grid squares to your leaflet maps.
Code inspiration from https://github.com/ablakey/Leaflet.SimpleGraticule/

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

    L.osGraticule().addTo(map);

```

Notes
-----
This is UK based grid, it will continue to display outwith the lat/lng bounds of the UK however it will become more and more distorted until at some point it stops displaying. 

To Do
-----
- Display labels including OS Grid letters and numbers
- Add configurable options
