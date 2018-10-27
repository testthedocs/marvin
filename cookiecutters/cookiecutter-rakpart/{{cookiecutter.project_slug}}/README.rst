{{ '=' * cookiecutter.project_name|length }}
{{cookiecutter.project_name}}
{{ '=' * cookiecutter.project_name|length }}

{{cookiecutter.short_description}}

Dependencies
============

- `Docker <https://docker.com>`_

Installation
============

Pull the image:

.. code-block:: shell

   docker pull testthedocs/{{cookiecutter.docker_image}}

Usage
=====

Run `{{cookiecutter.docker_image}}` from in your docs directory:

.. code-block:: shell

   docker run

Contribute
==========

- `Issue Tracker <https://github.com/testthedocs/rakpart/issues>`_
- `Source Code <https://github.com/testthedocs/rakpart/tree/master/{{cookiecutter.docker_image}}`_

Support
=======

If you are having issues, please let us know.

License
=======

`MIT <https://choosealicense.com/licenses/mit/>`_
