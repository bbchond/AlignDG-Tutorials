Installation
============

Software dependencies
---------------------
.. code-block:: python

   scanpy
   pytorch
   jax
   jaxlib
   


Installation
------------
1. Using conad and pip (We assume that you have installed Python or in conda virtual environment):

   We recommend users install PyTorch and Jax in previous if they have cuda devices. 

   To install Pytorch with cuda support, please visit: https://pytorch.org/get-started/locally.

   To install Jax (Jaxlib) with cuda support, please visit: https://docs.jax.dev/en/latest/installation.html.

   Please also install the necessary supported packages for Pytorch and PyG (https://pytorch-geometric.readthedocs.io/en/latest/install/installation.html) required by AlignDG: 

.. code-block:: python

   pip install pyg_lib torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-${TORCH}+${CUDA}.html

where ${TORCH} and ${CUDA} should be replaced by the specific PyTorch and CUDA versions, respectively:

PyTorch 2.8.*: ${TORCH}=2.8.0 and ${CUDA}=cpu|cu126|cu128|cu129

PyTorch 2.7.*: ${TORCH}=2.7.0 and ${CUDA}=cpu|cu118|cu126|cu128

PyTorch 2.6.*: ${TORCH}=2.6.0 and ${CUDA}=cpu|cu118|cu124|cu126

PyTorch 2.5.*: ${TORCH}=2.5.0 and ${CUDA}=cpu|cu118|cu121|cu124

PyTorch 2.4.*: ${TORCH}=2.4.0 and ${CUDA}=cpu|cu118|cu121|cu124

PyTorch 2.3.*: ${TORCH}=2.3.0 and ${CUDA}=cpu|cu118|cu121

PyTorch 2.2.*: ${TORCH}=2.2.0 and ${CUDA}=cpu|cu118|cu121

PyTorch 2.1.*: ${TORCH}=2.1.0 and ${CUDA}=cpu|cu118|cu121

PyTorch 2.0.*: ${TORCH}=2.0.0 and ${CUDA}=cpu|cu117|cu118

PyTorch 1.13.*: ${TORCH}=1.13.0 and ${CUDA}=cpu|cu116|cu117


After install the necessary packages, you can install AlignDG via pip:

.. code-block:: python

   pip install aligndg

Then, check install:

.. code-block:: python

   import aligndg
   print(aligndg.__version__)
   

2. From source code (Github):
   First, Download AlignDG code from https://github.com/xkmaxidian/AlignDG

   Then, cd your_path/aligndg

   Input: 

.. code-block:: python

   python setup.py build
   python setup.py install


