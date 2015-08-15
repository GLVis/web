# Building GLVis

A simple tutorial how to build and run GLVis together with MFEM. For more details, see the [INSTALL](https://raw.githubusercontent.com/glvis/glvis/master/INSTALL) file.

## Compilation

Download MFEM and GLVis (below we assume that we are working with versions 3.0)

  - [http://mfem.org](http://mfem.org)
  - [http://glvis.org](http://glvis.org)

Put everything in the same directory:
```sh
~> ls
glvis-3.0.tgz   mfem-3.0.tgz
```

Build the serial version of MFEM:
```sh
~> tar -zxvf mfem-3.0.tgz
~> cd mfem-3.0
~/mfem-3.0> make serial -j
```

Build GLVis:
```sh
~> tar -zxvf glvis-3.0.tgz
~> cd glvis-3.0
~/glvis-3.0> make MFEM_DIR=../mfem-3.0 -j
```

That's it! The `glvis` executable can be found in the `glvis-3.0` directory.

## Testing and rebuilding

To test the build, visualize a mesh with
```sh
~/glvis-3.0> ./glvis -m ../mfem-3.0/data/escher.mesh
```

To start a GLVis server, open a **new terminal** and start glvis without arguments
```sh
~/glvis-3.0> ./glvis
```

To rebuild GLVis after changes in MFEM (e.g. if MFEM has rebuild in parallel), do:

```sh
~/glvis-3.0> make clean
~/glvis-3.0> make MFEM_DIR=../mfem-3.0 -j
```
