marker_map
==========

A web server with only one javascript-loaded page written to mark your data points onto Google map.

How it works
------------

markers.html loads latitude-longitude pairs from a CSV (Comma Separated Value) file which includes headers, and then marks the coordinates on Google map.

Uses
----

The simplest way to use `marker_map` to start a basic web server at the folder.

``` bash
$ python -m SimpleHTTPServer 5000
```
**or** if you have installed `node.js` and `http-server` from `npm`:

``` bash
$ http-server -p 5000
```

**then** visit [http://localhost:5000/markers.html?csv=some_european_cities.csv](http://localhost:5000/markers.html?csv=some_european_cities.csv) in your favorite browser(s).

You can open remotely served CSV as well:
[http://localhost:5000/markers.html?csv=https%3A%2F%2Fdocs.google.com%2Fspreadsheet%2Fpub%3Fhl%3Den%26hl%3Den%26key%3D0Ah73xeahAckPdFRpUWl4cUZIZEFQRVlLbjB6RWFNamc%26output%3Dcsv](http://localhost:5000/markers.html?csv=https%3A%2F%2Fdocs.google.com%2Fspreadsheet%2Fpub%3Fhl%3Den%26hl%3Den%26key%3D0Ah73xeahAckPdFRpUWl4cUZIZEFQRVlLbjB6RWFNamc%26output%3Dcsv) which is [a list of red-light cameras' locations at Chicago][4] geocoded with [batch_geocode.py][batch_geocode].

You can also integrate it into your existing project.

[4]: https://docs.google.com/spreadsheet/pub?key=0Ah73xeahAckPdFRpUWl4cUZIZEFQRVlLbjB6RWFNamc&output=html
[batch_geocode]: https://github.com/falcondai/batch_geocode

Nice features
-------------

- Intuitive viewport. Auto pan-and-zoom to make all the markers visible at startup.
- Clean chart. Markers are automatically clustered to enhance readability.
- Informative. Each marker is clickable and a pop-up box will show all the information associated with that marker.
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