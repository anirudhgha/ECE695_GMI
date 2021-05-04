# ECE695_GMI
Class project codes and other related files. See powerpoint for more project details. 

## Running the project
There are two .ipynb files in the project folder, each contain everything necessary to run the metropolis simulations on H20 and Alanine dipeptide. The codes are written on top of a package openmmtools, that itself sits on openmm. These are separately installable. The environment file for the conda environment is provided in the project folder. They can be installed separately following the links below as well. 

http://docs.openmm.org/latest/userguide/application.html#installing-openmm
https://openmmtools.readthedocs.io/en/0.18.1/installation.html

## Project Description
Protein folding is a common problem tackled conventionally in the field of Molecular Dynamics. Recently, increases in computational power are allowing very fast random number generation, and by extension using Monte Carlo methods to solve problems that may previously been infeasable. Finding a low energy configuration for some set of atoms or particles would fall squarely in this category. 

Presented here are 2 simple codes that uses openmmtools to run the metropolis algorithm with a gaussian proposal distribution on pre-loaded test systems. These test systems provide a list of starting atoms, and the parameters specific to the particles that are required in the energy function (This is especially useful for the alanine-dipeptide example as there are ~21 atoms of different types).

1. The H20 molecule is a textbook system, for which the lowest energy state is known. The system is initialized with positions that are far from the ground state, and the system is allowed to evolve via the Metropolis-Hastings algorithm. The final state's dihedral bond angle is shown to be 104.02 degrees, which matches the known bond angle of 104.5 degrees for H20. 

2. The same algorithm is extended to a larger protein, Alanine Dipeptide, where a similar minimization in RMSD from the ground state is observed, and energy is also seen decreasing over the course of the M-H simulation. These results are presented in the powerpoint file. 





