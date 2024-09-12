# reactorFoam
Solver based on interFoam for 2 incompressible, isothermal immiscible fluids using a VOF     (volume of fluid) phase-fraction based interface capturing approach,     with optional mesh motion and mesh topology changes including adaptive     re-meshing.     The solver has option to calculate radiation decay of one of fluids. The solver is based on [OpenFOAM-v10](https://openfoam.org/version/10/).

## Physiscs
In the file **alphaEqn.H** we have added _+ lambda*alpha1_ that represent radioactive decay in the transport equation. This principle is base on the work of [Savovic et al.](https://doi.org/10.1093/rpd/ncr397).

## Instalation
    cd $HOME/OpenFOAM/<USER>-10
    mkdir applications
    cd applications
    mkdir solvers
    cd solvers
    git clone https://github.com/emirHanic/reactorFoam.git
    cd reactorFoam
    wmake