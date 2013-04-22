marker_map
==========

A web server with only one javascript-loaded page written to mark your data points onto Google map.

Uses
----

The simplest use to start a basic web server at the folder.

``` bash
$ python -m SimpleHTTPServer
```
or if you have installed `node.js` and `http-server` from `npm`:

``` bash
$ http-server -p 5000
```

then visit `localhost:5000/overlay.html?csv=sample.csv` in your favorite browser(s).

You can also integrate it into your existing project.

Nice features
-------------

- Intuitive viewport. Auto pan-and-zoom to make all the markers visible at startup.
- Clean chart. Markers are automatically clustered to enhance readability.
- Mobile ready. The size of the map is adjusted to fit mobile devices.

Dependencies
------------

- [d3js][1] used to parse input CSV files. (Released under BSD license)
- [markerclusterer][2] part of [google-maps-utility-library-v3][3], used to cluster markers. (Released under Apache 2.0 license)

[1]: http://d3js.org
[2]: https://code.google.com/p/google-maps-utility-library-v3/wiki/Libraries#Marker_Clusterer_Plus
[3]: https://code.google.com/p/google-maps-utility-library-v3/

License
-------

MIT License

Author
------

Falcon Dai