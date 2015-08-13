<div class="col-md-6" markdown="1">

[<img class="centered" src="img/logo-300.png" alt="GLVis logo">](gallery.md)

GLVis is a _lightweight_ OpenGL tool for _accurate_ visualization of _serial_ and _parallel_ finite element meshes and functions.

## Features

 * Accurate finite element mesh and function representation through interactive refinement.
 * [Server mode](options-and-general-use.md#server-mode) accepting multiple and/or persistent socket connections.
 * Support for triangular, quadrilateral, tetrahedral and hexahedral elements with [curved boundaries](mesh-formats.md#curvilinear-and-more-general-meshes).
 * 2D and 3D, arbitrary high-order H1, H(curl), H(div), L2 and [NURBS](NURBS.md) elements.
 * Visualization of [parallel](parallel-visualization.md) meshes and solutions.
 * ... and [many more](Features.md).

GLVis is based on the [MFEM](http://mfem.org) library and is currently used in the [BLAST](http://www.llnl.gov/casc/blast), _[hypre](http://www.llnl.gov/casc/hypre)_ and [XBraid](http://www.llnl.gov/casc/xbraid) projects. See also our [Gallery](gallery.md).

</div><div class="col-md-6" markdown="1">

## Latest Release

**
[New features](https://raw.githubusercontent.com/glvis/glvis/master/CHANGELOG)
/ [User documentation](https://raw.githubusercontent.com/glvis/glvis/master/README) 
/ [Code documentation](http://glvis.github.io/doxygen/html/index.html) 
/ [Sources](https://github.com/glvis/glvis)
**

[<button type="button" class="btn btn-success">
**Download glvis-3.0.tgz**
</button>](http://goo.gl/HcdvqY)

For older releases see the [download](download.md) section.

## Documentation

**
[Building GLVis](building.md) 
/ [Mesh formats](mesh-formats.md) 
/ [Parallel visualization](parallel-visualization.md) 
<br> [VTK meshes](vtk-meshes.md) 
/ [NURBS meshes and solutions](nurbs.md) 
**

The best starting point for new users is the [options and general use](options-and-general-use.md) tutorial.

We also recommend reading documentation for the [MFEM project](http://mfem.org).

## Contact

Developed by the [GLVis team](about.md) at [CASC](http://computation.llnl.gov/casc/),
[LLNL](https://www.llnl.gov/). Please cite with

    @misc{glvis-tool,
      title = {{GLVis}: Accurate finite element visualization},
      howpublished = {\url{glvis.org}}
    }

Use the GitHub [issue tracker](https://github.com/glvis/glvis/issues)
to report [bugs](https://github.com/glvis/glvis/issues/new?labels=bug)
or post [questions](https://github.com/glvis/glvis/issues/new?labels=question)
or [comments](https://github.com/glvis/glvis/issues/new?labels=comment).

</div>

<div class="col-md-12"></div>
