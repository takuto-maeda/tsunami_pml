# tsunami_pml
Perfectly matched layer absorbing boundary condition for simulation of
tsunami wave propagation

Corresponding Author: Takuto Maeda (maeda (at) eri.u-tokyo.ac.jp)

* * *

## Description

This software simulates tsunami wave propagation under the linear long wave
(LLW) and the liner dispersive wave (LDW) approximation with the perfectly
matched layer absorbing boundary condtion. The theory is fully described in
the accompanying paper:

Maeda, T., H. Tsushima, and T. Furumura,
paper-title,
journal,
doi:

The author request that the user to cite the above acompanying paper in any
publications that result from the use of this software, although this is
not an obligation.


## License

MIT


## Languages and Requirements

Fortran 2008

The author confirms it successfully work at the following compilers:
gfortran 5.1.0 (Mac OSX)
Intel fortran 2015 (Linux)


## How to use

The LLW and LDW models are given in separated programs (llw.f90 and ldw.f90).

They include the following three block files when they are compiled:

 * blk_param.f90: parameter for model size, grid width and the title for output
 * blk_initheight.f90: define the initial sea height
 * blk_bathymetry.f90: define the bathymetry
 * blk_station.f90: defnine number of station and station locations

After modification of these files, compile llw.f90 and/or ldw.f90.
Block files (blk_*.f90) are automatically included into the main program files.
It is not necessary to compile them separately.
