Getting started with Carrot
===========================

Introduction
------------

Carrot is a lightweight task queue backend for Django projects that uses the RabbitMQ message broker, with an emphasis
on quick and easy configuration and task tracking

Features
--------

- Minimal configuration required
- Task scheduling
- Task prioritization
- Task-level monitoring via the Carrot monitor
- Multithreaded queue consumers

Installation
------------

.. code-block:: bash

    pip install django-carrot


Configuration
-------------

1. Add carrot to your Django project's settings module:

.. code-block:: python

    INSTALLED_APPS = [
        ...
        'carrot',
        ...
    ]


2. Create the carrot migrations and apply them to your project's database:

.. code-block:: python

    python manage.py makemigrations carrot
    python manage.py migrate carrot

3. Set your default broker in your Django project's settings

.. code-block:: python

    CARROT = {
        'default_broker': 'amqp://guest:guest@localhost:5672
    }


Full documentation
------------------

The full documentation is available at `readthedocs.io <http://django-carrot.readthedocs.io/en/latest/index.html>`

Contribute
----------

- Issue Tracker: https://github.com/chris104957/django-carrot/issues
- Source Code: https://github.com/chris104957/django-carrot

Support
-------

If you are having any issues, please contact christopherdavies553@gmail.com

License
-------

The project is licensed under the Apache license.