jgir-fork
=========

An experimental fork of [java-gobject-introspection](https://wiki.gnome.org/Projects/JGIR) for [gstreamer-1.x-java](https://github.com/octachoron/gstreamer-1.x-java).

###Building

Building requires older versions of several jars:
 * [JNA 3.0.6](https://github.com/twall/jna/releases/tag/3.0.6)
 * [ASM 3.1](http://forge.ow2.org/project/download.php?group_id=23&file_id=9308)
 * [Stringtemplate 3.2.1](https://github.com/antlr/website-st4/blob/gh-pages/download/stringtemplate-3.2.1.tar.gz)

Put these in a directory under the project root called ```custom-jars```, and configure with

```
XDG_DATA_DIRS="$PWD/custom-jars:/usr/share" ./configure
```

```make``` and ```make install``` should work as usual. Installing into a custom directory is possible using

```
make DESTDIR=~/jgir-uninstalled install
```

This currently has a bug that causes a wrong jgir.jar path to be put on the classpath in the scripts.
