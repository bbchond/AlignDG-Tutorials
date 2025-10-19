Installation
============

Software Dependencies
---------------------
The following core dependencies are required:

.. code-block:: python

   scanpy
   numpy
   pandas
   anndata
   matplotlib
   scipy
   scikit-learn
   psutil
   cloudpickle
   tqdm
   leidenalg
   networkx
   docrep
   jax
   ott-jax[neural]
   torch
   torch-geometric
   wrapt
   rich
   plotly
   pyyaml
   torch-geometric
   torch-cluster
   torch-scatter
   torch-sparse

Installation Guide
------------------

1. Using Conda and Pip

We assume that you already have **Python** installed (preferably within a Conda virtual environment).

If you have CUDA-compatible devices, we recommend installing **PyTorch** and **JAX** with CUDA support beforehand.

- **To install PyTorch with CUDA support**, please follow the official guide:
  https://pytorch.org/get-started/locally

- **To install JAX (and JAXLIB) with CUDA support**, refer to:
  https://docs.jax.dev/en/latest/installation.html

Additionally, AlignDG requires several **PyTorch Geometric (PyG)** dependencies.  
It is strongly recommended to install these packages manually to avoid potential build issues (e.g., hanging at the `setup` step when installing `torch_cluster` via pip — a known issue).

Install the compatible PyG packages with the following command:

.. code-block:: bash

   pip install pyg_lib torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-${TORCH}+${CUDA}.html

Replace `${TORCH}` and `${CUDA}` with your specific PyTorch and CUDA versions, respectively.

For example, if you are using **PyTorch 2.8.0** with **CUDA 12.9**, run:

.. code-block:: bash

   pip install pyg_lib torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-2.8.0+cu129.html

Once all dependencies are installed, you can install **AlignDG** via pip:

.. code-block:: bash

   pip install aligndg

To verify the installation:

.. code-block:: python

   import aligndg
   print(aligndg.__version__)

---

2. From Source (GitHub)

You can also install AlignDG from source.

1. Clone the repository from GitHub:

   .. code-block:: bash

      git clone https://github.com/xkmaxidian/AlignDG.git

2. Navigate to the source directory:

   .. code-block:: bash

      cd your_path/AlignDG_package

3. Build and install the package:

   .. code-block:: bash

      python setup.py build
      python setup.py install

---

Notes
- We strongly recommend using **Python ≥ 3.10** and **pip ≥ 22.0**.
- To avoid dependency conflicts, always install AlignDG in a clean virtual environment (e.g., via Conda or `venv`).
- For GPU users, ensure that your CUDA toolkit and drivers are correctly configured before installing PyTorch/JAX.
