.. _main:

YOURLS Client
=========================================

This small library was created to provide an easy interface to YOURLS from
a python program.

Simple example of shortening a URL::

    import yourls.client

    c = yourls.client.YourlsClient('http://localhost/yourls/yourls-api.php', username='username', password='password')
    url = c.shorten('http://autoqa.fedorahosted.org/autoqa', keyword='autoqa')

News
-------------
There has been a change in how errors are thrown in 0.2.0, please see the API
documenatation for details.

Code Download
-------------
The code can be checked out from the github repository:
  * ``git clone git://github.com/tflink/python-yourls.git``

Or the code can be downloaded as a tarball from github:
  * https://github.com/downloads/tflink/python-yourls/python-yourls-0.2.0.tar.gz

Command Line
-------------
`python-yourls` also provides a command line interface.

Running tests
-------------
Running test units requires at least `YOURLS_TEST_TOKEN` environment 
variable to be set. Otherwise `test_token_shorturl_and_expand` will fail.

Here's an example on how to run unit tests::

    env YOURLS_TEST_TOKEN='my_yourls_token' python setup.py test

API Documentation
-----------------
.. automodule:: yourls
    :members:

.. automodule:: client
    :members:

.. autoclass:: YourlsClient
   :members:

.. toctree::
   :maxdepth: 2

   changelog

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

