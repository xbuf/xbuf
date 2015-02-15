xbuf is for [Protocol Buffers (aka protobuf)](https://developers.google.com/protocol-buffers/) Game Exchange. It's a data format usable to store scene in file or to edit scene over network. It takes inspiration from :
* [OpenGEX](http://opengex.org/) : as data to managed, and doc fragment I copied
* [glTF](https://github.com/KhronosGroup/glTF) : some discussion
* Entity-Component-System (ECS), RDF : as way to extends and to link data

License : [Public domain (CC0-1.0)](http://creativecommons.org/publicdomain/zero/1.0/)

# Use cases

* create importer/exporter for modeler, game engine, tool
* create network exchange format between connected tool (eg : modeler <-> game engine with realtime rendering)
  
  [![jme in blender](http://img.youtube.com/vi/3pQd65_dkeM/0.jpg)](http://www.youtube.com/watch?v=3pQd65_dkeM)

# Download

You can download files from [my repo](https://bintray.com/package/files/davidb/maven/xbuf)

* xbuf-x.y.z-proto.zip : archive with .proto files
* xbuf-x.y.z-cpp.zip : archive with generated C++ source
* xbuf-x.y.z-python.zip : archive with the xbuf modules (generated python)
* xbuf-x.y.z.jar : the java archive with generated .class

# Documentation

* [Motivations](https://github.com/davidB/xbuf/wiki/Motivations)
* [FAQ](https://github.com/davidB/xbuf/wiki/FAQ)
* [API](https://github.com/davidB/xbuf/wiki/API)
* [Extensions List](https://github.com/davidB/xbuf/wiki/Extensions-List)
* [Tools](https://github.com/davidB/xbuf/wiki/Tools)

# Links

* discussions about open format for 3D:
  * [Blender Artists: Alternative-to-FBX](http://blenderartists.org/forum/showthread.php?348506-Alternative-to-FBX/page3)
