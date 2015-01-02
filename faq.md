# FAQ

## What ...

### What are the units, coordinate system ?

* Coordinate system : Right Handled
  * object : Y up, Z forward, X left
  * camera : Y up, Z lookAt direction, X left
  * orthogonal-axes
  * uniform axis unit
  * front face: CCW (counter-clock-wise), back face: CW
* distance unit : meter
* time unit : second
* angle unit : radian

I try to collect same data for game engine, tools, to help create importer/exporter. Help me to complete the [table](https://docs.google.com/spreadsheets/d/19FscoJzidZKF6Iqs1bqELv57Ds-t_dAbMD_XflrIUuk/edit?usp=sharing)

### What is the file extension ?

```
.pgex
```

### What is the future of the format ?

I don't know ;-)

But there some ideas :

* integrate some community' suggestions
* ingrate compression  like [glTF: Open 3D Graphics Compression](https://github.com/KhronosGroup/glTF/wiki/Open-3D-Graphics-Compression)
* define an archive format to store complementary data : textures, shaders, ...

## How ...

### How can I protect my content ?

1. change the file extension
2. modify the file content, example of modifications (can be combined) :
  * wrap into your own proto Message
  * add an header at the begin of the file (a fixed or variable size of useless bytes, some license info)
  * encrypt : rot13, pgp, ...
  * wrap into an archive (but without the reguler extension): tar, zip,...
  * compress (but without the reguler extension) : snappy, gzip, bzip, lzma,...

## Why ...

### Why not OpenGEX ?

* require to write parser, loader, exporter
* text based, not optimal for network and realtime update

### Why not [glTF](https://github.com/KhronosGroup/glTF) ?

* moving and heavy spec ;-)
* json based, require to write "semantic" parser, converter.

### Why no configurable metrics (like in OpenGEX) ?

* to simplify the loader (less combinaison, less confusion) : *"convention over configuration"*
* to ease share and merge of data
* it's the responsability of the exporter to write sharable data (from internal format to pgex)

see discussion [glTF : unify scenes axis-up](https://github.com/KhronosGroup/glTF/issues/22)

## Why no configurable up ?

* see *Why no configurable metrics (like in OpenGEX) ?* (above)
* To avoid branch in loader code like in this [response on unity forum](http://answers.unity3d.com/questions/46589/zup-yup-xup-handedness-space-conversion.html)

### Why no transform matrix, variant of Rotation, Scale ?

* see *Why no configurable metrics (like in OpenGEX) ?* (above)
* I don't want too freedom (simple loader, more work on exporter), so I have to choose between matrix or translation / rotation / scale
* Extracting translation / rotation / scale from a 4×4 matrix is harder than creating a 4×4 matrix from translation / rotation / scale is much easier.
