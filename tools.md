# Existing Tools, Libraries, ...

# Ideas for Tools

## Checker

* in a collection of datas (.pgex) : verify that every ref points to existing id.
* in a collection of datas (.pgex) : verify (+ correct) order of the ref in Relation.
* in a datas (.pgex) : verify that size of XxxBuffer is a multiple of its step.
* in a datas (.pgex) : verify that every rpath points to existing file in assets' folder.

## Merge

* merge a collection of datas into a single datas + external assets

# Extractor

* from a collection of datas (.pgex) : extract Node and related data + assets into its own datas
* from a collection of datas (.pgex) : extract Material and related data + assets into its own datas
* from a collection of datas (.pgex) : list all assets (rpath)

# Remapper

* in a collection of datas (.pgex) : rename id (and ref) (via regexp or conversion table or a generator)
* in a collection of datas (.pgex) : change rpath (and ref) (via regexp or conversion table)
