|Travis|_ |Codecov|_

.. |Travis| image:: https://travis-ci.org/xofbd/discrete-fracture-network.svg?branch=master
.. _Travis: https://travis-ci.org/xofbd/discrete-fracture-network

.. |Codecov| image:: https://codecov.io/gh/xofbd/discrete-fracture-network/branch/master/graph/badge.svg
.. _Codecov: https://codecov.io/gh/xofbd/discrete-fracture-network

Discrete Fracture Network
=========================
An analytical thermohydraulic model for discretely fractured geothermal
reservoirs. This package is an implementation of the model described in
Fox, D. B., D. L. Koch, and J. W. Tester (2016), An analytical thermohydraulic
model for discretely fractured geothermal reservoirs, Water Resources Research,
52, 6792-6817, doi:10.1002/2016WR018666

Prerequisites
-------------
You will need to have the following Python packages installed:
``networkx, numpy, scipy``.
You can easily download and install these packages by running ``pip install package-name``, where "package-name" is the name of the desired package.

Installing
----------
To install the package, clone the repo and run ``python setup.py install`` or ``make install``

Usage
-----
Here is a short example of creating a simple network.
  >>> import dfn
  >>> conn = [(0, 1), (1, 2), (1, 2), (2, 3)]
  >>> L = [100., 500., 500., 100.]
  >>> H = [500., 500., 500., 500.]
  >>> w = [1E-3, 1E-3, 1E-3, 1E-3]
  >>> network = dfn.FractureNetwork(conn, L, H, w)

For more extensive examples of usage, look at the scripts in the ``example`` directory.

Tests
-----
There are several files in the ``dfn/test`` that perform unit testing. You can run those tests by running ``make test``

License
-------
This project is distributed under the MIT license. Please see ``LICENSE`` for more information
