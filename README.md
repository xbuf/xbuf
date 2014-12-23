pgex is for [Protocol Buffers (aka protobuf)](https://developers.google.com/protocol-buffers/) Game Exchange. It's a data format usable to store scene in file or to edit scene over network. It takes inspiration from [OpenGEX](http://opengex.org/) and [glTF](https://github.com/KhronosGroup/glTF).

License : [Public domain (CC0-1.0)](http://creativecommons.org/publicdomain/zero/1.0/)

# Why ?

* .proto is used as spec and to generate generator/parser for several languages. No need to write your own (you can if you want). And tool, game, engine spend less time on creating generator/parser. Developper only need to create adapter, converter into their own format (far easier than creating generator + parser).
* protobuf have support for lot of programming language (my priority order):
  1. python : blender exporter, realtime renderer is my first target as tool.
  2. c/c++, java : lot of tools, game-engine are writen in C/C++ and jmonkeyengine are my first target as game engine.
  3. go, rust, dart, javascript : are used by lot of game engine (maybe the future).
  4. c# : used by unity3d
* type checking (at compile time or runtime) is developper friendly.
* often protobuf will generate better parser (error reporting) than hand written.
* a realy open/free format with source, doc hosted on public repository (github)
* protobuf have an ecosystem, port, ide support,...


## Comments

* file are binary, not text.
  * pros : size
  * cons : impossible to read or to edit content with a text editor
* Why not, flatbuffers, capnproto ? because not mature/developper friendly enough for my first target language (python, java, c/c++), may be for an other adaptation
* Why not, msgpack, json, yaml,... ? they require to write doc spec, and to create generator/parser. Same issue than OpenGEX and ODDL.
* Protobuf is not the best in size of the content, or the best is performence (reading/writing), has code generator,... but it's the optimal for my target (see 'Why ?')
* Quality for protoc plugins is very variable between language. Some languages have several generators (eg: python, c#).
* For python3 I need to convert the package protobuf-2.6.1 to python 3 (via a simple script)
* Using an intermediary (pivot) format generate lot of copy (eg: conversion from internal vec3 to pgex vec3) :overhead at coding time and runtime.


# Use cases

* create importer/exporter for modeler, game engine, tool
* create network exchange format between connected tool (eg : modeler <-> game engine with realtime rendering)

# Links

* discussions about open format for 3D:
  * [Blender Artists: Alternative-to-FBX](http://blenderartists.org/forum/showthread.php?348506-Alternative-to-FBX/page3)
