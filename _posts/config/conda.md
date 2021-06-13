---
title: Conda
---

```bash
conda --version  # version number
conda info  # conda installation info
conda update conda  # update conda

conda create -n py_3_6_8 python=3.6.8
conda list --explicit > requirements.txt  # produce a spec list
conda create -n py_3_6_8 --file requirements.txt -c conda-forge  # packages in requirements

conda env list  # list all virtual evnironments
conda info --envs  # list all virtual evnironments
conda activate py_3_6_8  # use py_3_6_8
conda deactivate  # quit py_3_6_8
conda list  # list installed packages
conda list -n py_3_6_8  # installed packages under py_3_6_8
conda search numpy  # search numpy
conda install -n py_3_6_8 numpy  # install numpy under py_3_6_8
conda remove [-n py_3_6_8] numpy  # remove package
conda update [-n py_3_6_8] numpy  # update package
conda remove --name py_3_6_8 --all  # remove py_3_6_8
conda env remove --name py_spark

conda clean -h

conda env export -n tf1.4 --file conda_env.yml
```