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


Packaged from https://github.com/fanzheng10/CliXO Original paper: Kramer M, Dutkowski J, Yu M, Bafna V, Ideker T. Inferring gene ontologies from pairwise similarity data. Bioinformatics, 30: i34-i42. 2014. doi: 10.1093/bioinformatics/btu282

* A classical method that iteratively detects hierarchy based on cliques from changing edge weight threshold.
* CliXO only works on graph with edge weights.
* For reasonable runtime, the maximum size of network is of hundreds of nodes.

* Parameter `alpha`: threshold between cluster layers (default `0.1`)
* Parameter `beta`: merge similarity for overlapping clusters (default `0.5`)

Features
--------

* TODO

Credits
---------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
