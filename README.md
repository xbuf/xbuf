xbuf is an exchange format usable to store scene, models, animations in file or to edit scene over network. It takes inspiration from :

* [OpenGEX](http://opengex.org/) : as data to managed, and doc fragment I copied
* [glTF](https://github.com/KhronosGroup/glTF) : some discussions and some goals
* [blender api](http://www.blender.org/api/blender_python_api_2_72_release/) : how blender manages data
* Entity-Component-System (ECS), RDF : as way to extends and to link data

xbuf is a binary format using [Protocol Buffers (aka protobuf)](https://developers.google.com/protocol-buffers/) to generate source code for java, C++, python,... to read and write it. Then it's more developer friendly than json, oddl, xml, or any text based dialect, without loosing flexibility via extension.

The project would like to be an **Community Format** shared by several engines, tools. It's **Open** to any contributions (code, discussion, issues, tools, ...).

License : [Public domain (CC0-1.0)](http://creativecommons.org/publicdomain/zero/1.0/)

[![Standards](http://imgs.xkcd.com/comics/standards.png)](http://xkcd.com/927/)

# Use cases

* create importer/exporter for modeler, game engine, tool (optimizer, asset pipes...)
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

* discussions about xbuf in communities:
  * jMonkeyEngine : [Xbuf format – A developper friendly game exchange format for 3d data](http://hub.jmonkeyengine.org/t/xbuf-format-a-developper-friendly-game-exchange-format-for-3d-data/31130/19)
  * Ogre3D : [Ogre Forums • View topic - xbuf: call for help for an other 3D format](http://www.ogre3d.org/forums/viewtopic.php?f=1&t=82801&p=514877#p514877)
* discussions about open format for 3D:
  * [Blender Artists: Alternative-to-FBX](http://blenderartists.org/forum/showthread.php?348506-Alternative-to-FBX/page3)


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/xbuf/xbuf/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

