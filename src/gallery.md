# Gallery

This page collects screenshots from various simulations that have used GLVis visualization. Additional images can be found in the [MFEM Gallery](http://mfem.org/gallery).

<br>
<center>

<div class="col-md-4"  markdown="1">

[![](img/gallery/logo-gallery.png)](img/gallery/logo-gallery-full.png)

*The GLVis logo is derived from the [Metatron model](http://www.bathsheba.com/downloads/metatron.zip) at [bathsheba.com](http://www.bathsheba.com). Shown is the magnitude of the projection of a smooth vector field using 4th order Nedelec elements on a second order curved tetrahedral mesh (based on MFEM's [Example 3](http://mfem.github.io/doxygen/html/ex3_8cpp_source.html)).*

----

![](img/gallery/triple-pt-rz-2-web.png)

*Axisymmetric problem with revolved 2D mesh and solution, plus [coloring grid functions](options-and-use.md#visualizing-functions) emphasizing mesh elements. See also the [video](https://youtu.be/SxKHWlKIIOs).*

----

![](img/gallery/ball-nurbs-np16.png)

*Unstructured parallel decomposition of a [fourth order NURBS mesh](https://github.com/mfem/mfem/blob/master/data/ball-nurbs.mesh) of the unit ball obtained in the solution of MFEM's parallel [Example 1](https://github.com/mfem/mfem/blob/master/examples/ex1p.cpp) on 16 processors.*

----

[![](img/gallery/quadrature-lor.png)](img/gallery/quadrature-lor.png)

*Quadrature data visualization on a [low-order-refined](https://mfem.org/tutorial/solvers/#low-order-refined-methods) (LOR) mesh. Several different visualization options are available via key 'Q'.*

----

![](img/gallery/q8.png)

*One of the eight order (Q8) basis functions on the reference square. The sub-refinement in GLVis (key 'i') allows for the correct visualization of such high-order functions.*

----

![](img/gallery/sculpture-ar.jpg)

*GLVis model opened in augmented reality with the [glTF model viewer](https://modelviewer.dev/editor).*

</div><div class="col-md-5"  markdown="1">

[![](img/gallery/triple-point_BLAST_q8q7.png)](img/gallery/triple-pt-np128.gif)

*Curvilinear 8th order mesh from a triple-point shock simulation in the MFEM-based  [BLAST](http://www.llnl.gov/casc/blast) shock hydrodynamics code. Click for a movie of the evolution of the processor partitioning from a high-resolution parallel run of the problem produced with a [GLVis script](options-and-use.md#glvis-scripts).*

----

[![](img/gallery/sculptures.jpg)](img/gallery/sculptures-full.jpg)

*Raytraced glTF model in Blender which was exported from GLVis with the 'G' key. The mesh faces have been cut with 'Ctrl+F3'*

----

[![](img/gallery/tp-3d-ale-black.png)](http://computation.llnl.gov/)

*3D Arbitrary Lagrangian-Eulerian (ALE) simulation of a shock-triple point interaction with Q2-Q1 elements in the MFEM-based [BLAST](http://www.llnl.gov/casc/blast) shock hydrodynamics code. Shown are the cutting plane and level surface capabilities of GLVis.*

----

[![](img/gallery/partition-2048-a.png)](img/gallery/partition-2048-a.png)

*Parallel partitioning of a non-conforming adaptively refined mesh between 2048 processors based on splitting a space-filling (Hilbert) curve.*

----

![](img/gallery/fem2d-2.png)

*Level lines in 2D. Simulation with [MFEM](http://mfem.org).*

</div><div class="col-md-3"  markdown="1">

![](img/gallery/CSE13logo.jpeg)

*The [SIAM CSE13](http://www.siam.org/meetings/cse13) logo illustrates the decomposition of a hexahedral zone in tetrahedral "sides". This and related images can be found in [this paper](http://dx.doi.org/10.1137/100801640).*

----

[![](img/gallery/ex4-2.jpg)](img/gallery/ex4-2-full.png)

*The vector field solution of grad-div problem on a periodic mesh computed with hybridized 3rd order Raviart-Thomas elements. Lines correspond to backward Cartesian displacements (key 'd' in GLVis).*

----

![](img/gallery/hypre-ex4-np36-n15-K3-C1-U02-F4.png)

*Stitched parallel results from [hypre](http://www.llnl.gov/casc/hypre)'s Example 4 on 36 processors.*

----

[![](img/gallery/NURBS-ball-impact1.jpg)](img/gallery/NURBS-ball-impact1-full.png)

*The solution of the Laplace problem on a 3D [NURBS](nurbs.md) mesh. Shown are the solution values in a cutting plane and one of the internal boundaries.*

----

![](img/gallery/fem2d-1.png)

*Locally refined grid in 2D. Simulation with [MFEM](http://mfem.org).*

</div>

</center>
