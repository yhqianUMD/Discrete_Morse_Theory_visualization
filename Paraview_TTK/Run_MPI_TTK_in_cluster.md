# Steps to run MPI-supported TTK on a cluster
* load necessary modules
  ```
  module load openmpi/3.1.0
  module load gcc/12.3.0
  module load boost/1.84.0 (may not necessary)
  ```
* go to the directory where ttk-paraview is installed
  ```
  cd /local/data/yuehui/local_yh/ttk-paraview/build/bin
  ```
* compute discrete gradient
  ```
  OMP_NUM_THREADS=6 mpirun -n 20 pvbatch pipeline.py
  ```
