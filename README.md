shapefile
==============

I modify the code for gmap and Openlayers 3.

Copyright [Kenneth Hu](http://www.kennethhu.net/)



**demo:**
[Google map](http://kennethhutw.github.io/demo/js2shapefile/gmap_sample.html)

![Image](https://raw.githubusercontent.com/kennethhutw/js2shapefile/master/gmap.gif)

[OSM map by Openlayers](http://kennethhutw.github.io/demo/js2shapefile/ol_sample.html)
  
![Image](https://raw.githubusercontent.com/kennethhutw/js2shapefile/master/olmap.gif)

A binary shapefile loader and canvas-based renderer, for javascript. Many caveats:

Seems best in Safari... times out in IE and in Firefox 3.5 with large files. 
Does the dumbest thing possible and reads entire shp and dbf files in one go.
Error checking is strange (needs testing with more known-good files). 
Implies that it's a good idea to load large binary files over the network. 
Only supports a small subset of shapes.
Is almost entirely negligent of the format specifications.
Doesn't do anything much apart from proof of concept.

http://www.nihilogic.dk/labs/binaryajax/binaryajax.js is used for loading binary data via XMLHttpRequest
http://code.google.com/p/vanrijkom-flashlibs/ was ported to js from actionscript
http://code.google.com/p/explorercanvas/ is used for IE support

dbf.js and shapefile.js are close relatives of the vanrijkom-libs code and as such are LGPL v2 as well
binarywrapper.js is new, to support parsing doubles and to keep track of binary offsets and endianness

excanvas.js is under Apache License 2.0
binaryajax.js is under MPL

world borders shapefile is from http://thematicmapping.org/downloads/world_borders.php licensed CC-BY-SA 3.0
