# Mapbox IOS SDK Wrapper for Titanium

Uses the [Mapbox iOS SDK](https://github.com/mapbox/mapbox-ios-sdk) `develop` branch.

## Use

Put the zip in your project, and add a reference in tiapp.xml.

### example/app.js

```javascript
var mapbox = require('com.polancomedia.mapbox');

var mapView = mapbox.createView({
    map: 'control-room',
    //map: 'road-trip',
    minZoom: 0,
    maxZoom: 6,
    zoom: 10,
    centerLatLng: [20.7972,-88.1598],
    width: Ti.UI.FILL,
    height: Ti.UI.FILL
});

win.add(mapView);
win.open();
```

### Sample Maps
The `example` folder contains two sample mbtiles maps:

#### control-room
* Zoom levels 0 through 6
* Full-world coverage

#### road-trip
* Zoom levels 7 through 12
* Only contains subset of world coverage

## Properties

`map`
* Required, path to local mbtiles file.

`debugTiles`
* Optional, defaults to false.

`hideAttribution`
* Optional, defaults to false.
* See Mapbox [Terms and Conditions](https://www.mapbox.com/mapbox-ios-sdk/#attribution) for attribution info.

## Todos
* Need to verify that min, max and default zoom levels work for maps that don't contain full-world (like road-trip).
* Add support for remote maps
* Add support for markers and other SDK items
* Contributions welcome

## About
Me: [Adam Paxton](http://adampaxton.com) 
Twitter: [@adampax](http://twitter.com/adampax)
Company: [Polanco Media, LLC](http://polancomedia.com)

## License
MIT License
Copyright (c) 2013 Polanco Media, LLC

Uses MapBox iOS SDK, (c) 2008-2013 MapBox and Route-Me Contributors
