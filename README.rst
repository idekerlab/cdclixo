===================================================
Community Detection CliXO
===================================================

.. image:: https://img.shields.io/pypi/v/cdclixo.svg
        :target: https://pypi.python.org/pypi/cdclixo

.. image:: https://img.shields.io/travis/idekerlab/cdclixo.svg
        :target: https://travis-ci.org/idekerlab/cdclixo

.. image:: https://readthedocs.org/projects/cdclixo/badge/?version=latest
        :target: https://cdclixo.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://requires.io/github/idekerlab/cdclixo/requirements.svg?branch=master
        :target: https://requires.io/github/idekerlab/cdclixo/requirements?branch=master
        :alt: Dependencies

This repository creates a CDAPS compatible community detection Docker image using CliXO
packaged from https://github.com/fanzheng10/CliXO

Original paper: Kramer M, Dutkowski J, Yu M, Bafna V, Ideker T. Inferring gene ontologies from pairwise similarity data. Bioinformatics, 30: i34-i42. 2014. doi: 10.1093/bioinformatics/btu282

* A classical method that iteratively detects hierarchy based on cliques from changing edge weight threshold.
* CliXO only works on graph with edge weights.
* For reasonable runtime, the maximum size of network is of hundreds of nodes.

* Parameter `alpha`: threshold between cluster layers (default `0.1`)
* Parameter `beta`: merge similarity for overlapping clusters (default `0.5`)

Dependencies
------------

* `Docker <https://www.docker.com/>`_
* `make <https://www.gnu.org/software/make/>`_ (to build)
* Python (to build)

Direct invocation
------------------

Version `0.1.0` can be directly pulled from `Dockerhub <https://hub.docker.com/>`_ with this command:

.. code-block::

   docker pull coleslawndex/cdclixo:0.1.0

Building
--------

.. code-block::

   git clone https://github.com/idekerlab/cdclixo
   cd cdclixo
   make dockerbuild

Run **make** command with no arguments to see other build/deploy options including creation of Docker image

.. code-block::

   make

Output:

.. code-block::

   clean                remove all build, test, coverage and Python artifacts
   clean-build          remove build artifacts
   clean-pyc            remove Python file artifacts
   clean-test           remove test and coverage artifacts
   lint                 check style with flake8
   test                 run tests quickly with the default Python
   test-all             run tests on every Python version with tox
   coverage             check code coverage quickly with the default Python
   docs                 generate Sphinx HTML documentation, including API docs
   servedocs            compile the docs watching for changes
   testrelease          package and upload a TEST release
   release              package and upload a release
   dist                 builds source and wheel package
   install              install the package to the active Python's site-packages
   dockerbuild          build docker image and store in local repository
   dockerpush           push image to dockerhub


Usage
-----

.. code-block::

   docker run -v coleslawndex/cdclixo:0.1.0 -h

Credits
---------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
