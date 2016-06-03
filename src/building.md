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

## Using secure sockets

As of version 3.2, GLVis can be built with support for secure sockets using the
[GnuTLS library](https://gnutls.org) through MFEM's `class socketstream`. This
option may be useful in multi-user environment to prevent users from
sending/receiving visualization data to/from other users. To enable this
support, first configure MFEM version 3.2 or later with
```sh
~/mfem-3.2> make config MFEM_USE_GNUTLS=YES
```
For more details consult MFEM's
[`INSTALL`](https://raw.githubusercontent.com/mfem/mfem/master/INSTALL) file.
After configuration, build MFEM and GLVis as usual:
```sh
~/mfem-3.2> make -j
~/mfem-3.2> cd ../glvis-3.2
~/glvis-3.2> make clean && make MFEM_DIR=../mfem-3.2 -j
```

In order to use the secure sockets with the GLVis server and client applications
like MFEM's
[Example 1](https://raw.githubusercontent.com/mfem/mfem/master/examples/ex1.cpp),
one needs to generate GLVis server and client key pairs. The simplest way to do
that is to use the
[`glvis-keygen.sh`](https://raw.githubusercontent.com/glvis/glvis/master/glvis-keygen.sh)
script in the main GLVis directory:
```sh
~/glvis-3.2> bash glvis-keygen.sh "User Name" "user@host.org"
```
The key generation requires the `gpg2` tool from [GnuPG](https://gnupg.org/).
The generated keys are saved in `~/.config/glvis/server` and
`~/.config/glvis/client`.

With this option enabled, GLVis will use secure sockets by default, as indicated
by the additional message after the logo:
```text
~/glvis-3.2> ./glvis

       _/_/_/  _/      _/      _/  _/
    _/        _/      _/      _/        _/_/_/
   _/  _/_/  _/      _/      _/  _/  _/_/
  _/    _/  _/        _/  _/    _/      _/_/
   _/_/_/  _/_/_/_/    _/      _/  _/_/_/

Generating DH params (1024 bits) ... done.
Waiting for data on port 19916 ...
```

The secure sockets can be disabled with the `-no-sec` or `--standard-sockets`
command line options.
