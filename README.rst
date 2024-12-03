===================
CAMB
===================
:CAMB: Code for Anisotropies in the Microwave Background
:Author: Antony Lewis and Anthony Challinor
:Homepage: https://camb.info/

.. image:: https://img.shields.io/pypi/v/camb.svg?style=flat
   :target: https://pypi.python.org/pypi/camb/
.. image:: https://img.shields.io/conda/vn/conda-forge/camb.svg
   :target: https://anaconda.org/conda-forge/camb
.. image:: https://readthedocs.org/projects/camb/badge/?version=latest
   :target: https://camb.readthedocs.io/en/latest
.. image:: https://github.com/cmbant/camb/actions/workflows/tests.yml/badge.svg?branch=master
  :target: https://github.com/cmbant/CAMB/actions
.. image:: https://mybinder.org/badge_logo.svg
  :target: https://mybinder.org/v2/gh/cmbant/CAMB/HEAD?filepath=docs%2FCAMBdemo.ipynb

Description and installation
=============================

CAMB is a cosmology code for calculating cosmological observables, including
CMB, lensing, source count and 21cm angular power spectra, matter power spectra, transfer functions
and background evolution. The code is in Python, with numerical code implemented in fast modern Fortran.

See the `CAMB python example notebook <https://camb.readthedocs.io/en/latest/CAMBdemo.html>`_ for a
quick introduction to how to use the CAMB Python package.

This is a modification of the original CAMB code by Dong Ha Lee for a more general parameterisation of dark energy equation of state.

To install, first clone the repository::

    git clone --recursive https://github.com/dlehdgk/CAMB_DE_beta.git

Then install an editable version of the python wrapper using::

    pip install -e .

In the source directory.
May need to clean the installation using::
    
    python setup.py clean

before re-installing if you have previously installed a different version.
If installing as part of [COBAYA](https://cobaya.readthedocs.io/en/latest/) to use a modified version of CAMB without creating a new environment each time, you can use::

    python setup.py build

You will need gfortran 6 or higher installed to compile (usually included with gcc by default).
If you have gfortran installed, "python setup.py make" (and other standard setup commands) will build the Fortran
library on all systems (including Windows without directly using a Makefile).

The python wrapper provides a module called "camb" documented in the Python `CAMB documentation <https://camb.readthedocs.io/en/latest/>`_.

After installation you can also run CAMB from the command line reading parameters from a .ini file, e.g.::

  camb inifiles/planck_2018.ini

To compile the Fortran command-line code run "make camb" in the fortran directory. For full details
see the  `ReadMe <https://camb.info/readme.html>`_.


.. raw:: html

    <a href="https://www.sussex.ac.uk/astronomy/"><img src="https://cdn.cosmologist.info/antony/Sussex_white.svg" style="height:200px" height="200px"></a>
    <a href="https://erc.europa.eu/"><img src="https://cdn.cosmologist.info/antony/ERC_white.svg" style="height:200px" height="200px"></a>
    <a href="https://stfc.ukri.org/"><img src="https://cdn.cosmologist.info/antony/STFC_white.svg" style="height:200px" height="200px"></a>
