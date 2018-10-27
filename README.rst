======
Marvin
======

Our robot for template creation, works with `Cookiecutter <https://cookiecutter.readthedocs.io/en/latest/index.html>`_.

Features
========

Creates templates, according to our setup and style-guide

List Of Templates
-----------------

- Boilerplate for `Rakpart <https://rakpart.testthedocs.org>`_ checks.

Dependencies
============

- `Docker <https://docker.com>`_

Installation
============

.. code-block:: shell

   docker pull testthedocs/marvin

Usage
=====

Change into the directory where you want to create the new *boilerplate*.

Run the following command to create the base setup for a new `Rakpart <https://rakpart.testthedocs.org>`_ check.

.. code-block:: shell

   docker run -it -v `pwd`:/srv/data testthedocs/marvin create-rakpart-check

Contribute
==========

- `Issue Tracker <https://github.com/testthedocs/marvin/issues>`_
- `Source Code <https://github.com/testthedocs/marvin>`_

Support
=======

If you are having issues, please let us know.

License
=======

`MIT <https://choosealicense.com/licenses/mit/>`
