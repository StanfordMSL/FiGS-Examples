# FiGS-Examples
Installation steps
1) Update submodules
```
git submodule update --recursive --init
```
2) Install acados
```
# Navigate to acados folder
cd <repository-path>/FiGS-Examples/FiGS/acados/

# Compile
mkdir -p build
cd build
cmake -DACADOS_WITH_QPOASES=ON ..
make install -j4

# Add acados paths to bashrc
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:"<acados_root>/lib"
export ACADOS_SOURCE_DIR="<acados_root>"
```
3) Setup conda environment (in the main directory)
```
# Navigate to environment config location
cd <repository-path>/FiGS-Examples/

# Create and activate
conda env create -f environment_x86.yml
conda activate figs-env
```
4) Download Example GSplats
```
# Navigate to gsplats parent folder
cd <repository-path>/FiGS-Examples/

# Use gdown to download
gdown --folder https://drive.google.com/drive/folders/1Q3Jxt08MUev_jWzHjpdltze7X4VArsvA?usp=drive_link --remaining-ok

# Alternatively, you can download the zip-ed file below and unpack the contents (capture and workspace) into the gsplats folder
https://drive.google.com/file/d/1kW5dzsfD3rbRA3RIQDyJPG6_UJaO9ALP/view
```
