# TRIQS with its supported impurity solvers

Container image available at 
* [Docker](https://hub.docker.com/r/triqs-full) ``docker pull fulvwen/triqs-full:gcc-mpich``
* [Github Packages](https://github.com/lyuwen/triqs-docker/pkgs/container/triqs-full) ``docker pull ghcr.io/lyuwen/triqs-full:gcc-mpich``

## Available list:
* CTHYB
* Pomerol
* NRG Ljubljana
* Hubbard I
* Hartree Fock
* W2dynamics

## Usage

* Use within docker
    ```bash
    docker run -ti --rm -v $PWD:/work --workdir /work fulvwen/triqs-full:gcc-mpich python3 script.py
    ```

* Use with Singularity
    ```bash
    singularity build triqs-full-gcc-mpich.sif docker://fulvwen/triqs-full:gcc-mpich
    ```
    1. use singularity interactively
        ```bash
        singularity shell --bind /home triqs-full-gcc-mpich.sif
        ```
    2. execute command directly with singularity
        ```bash
        mpirun -n 4 singularity exec --bind /home triqs-full-gcc-mpich.sif python3 script.py
        ```
