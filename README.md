# FiGS-Examples
Installation steps
1) Update submodules
```
git submodule update --recursive --init
```
2) Install acados
```
cd FiGS/acados/

mkdir -p build
cd build
cmake -DACADOS_WITH_QPOASES=ON ..
make install -j4

# Add acados paths to bashrc
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:"<acados_root>/lib"
export ACADOS_SOURCE_DIR="<acados_root>"
```
3) Setup conda environment and download gsplat examples
```
#  In main directory (where gsplats is a subdirectory)
conda env create -f environment_x86.yml
conda activate figs-env

gdown --folder https://drive.google.com/drive/folders/1Q3Jxt08MUev_jWzHjpdltze7X4VArsvA?usp=drive_link --remaining-ok
```