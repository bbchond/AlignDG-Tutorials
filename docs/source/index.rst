AlignDG: Alignment of spatial transcriptomics slices across diseases, platforms and conditions
====================================================================================================================================================


.. toctree::
   :maxdepth: 1

   Installation
   Tutorial_Simulation
   Tutorial_DLPFC


Overview of AlignDG
========================     
.. image:: AlignDG.png
   :width: 600

Installation
============ 

Note: AlginDG is built based on PyTorch and Jax. If you have an NVIDIA GPU, be sure to firstly install a version of PyTorch that supports it (We recommend Pytorch >= 2.0.1). When installing AlignDG without install Pytorch and Jax previous, the CPU version of PyTorch and Jax will be installed by default for you. Here is the [installation guide of PyTorch](https://pytorch.org/get-started/locally/) and  [installation guide of Jax](https://docs.jax.dev/en/latest/installation.html)

1. Start by using python virtual environment with conda (https://anaconda.org/):

.. code-block:: python

   conda create --name aligndg_py python=3.10
   conda activate aligndg_py
   pip install aligndg

(Optional) To run the notebook files in tutorials, please ensure the Jupyter package is installed in your environment:

.. code-block:: python

   conda install -n aligndg_py ipykernel
   python -m ipykernel install --user --name aligndg_py --display-name aligndg-jupyter

Note: If you encounter the error message "ImportError: Please install the skmisc package via `pip install --user scikit-misc`" while executing `sc.pp.highly_variable_genes(adata, flavor='seurat_v3', n_top_genes=3000)`, please execute the following command in your terminal: `pip install --user scikit-misc`.

2. Install AlignDG from GitHub (Not recommend)

.. code-block:: python

   git clone https://github.com/xkmaxidian/AlignDG
   cd <your dir path>/AlignDG/AlignDG_package
   python setup.py build
   python setup.py install

Note: The torch-geometric library is also required, please see the installation steps in https://github.com/pyg-team/pytorch_geometric#installation


Citation
========
Our paper is under review.
