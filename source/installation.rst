============
Installation
============


Server Requirements
===================

The Magister 6 API has a few system requirements.

You will need to make sure your server meets the following requirements:

- PHP >= 5.4.0
- cURL PHP Extension
- Mcrypt PHP Extension
- OpenSSL PHP Extension


Installing the Magister 6 API
=============================

The Magister 6 API utilizes `Composer <https://getcomposer.org>`_ to manage its dependencies. So, before using it, make sure you have Composer installed on your machine.

You can add the Magister 6 API as a dependency using the Composer CLI:

.. code-block:: bash

	composer require stanvk/magister-api ~2.0

Alternatively, you can specify the Magister 6 API as a dependency in your project's existing composer.json file:

.. code-block:: js

	{
	   "require": {
	      "stanvk/magister": "~2.0"
	   }
	}

After installing, you need to require Composer's autoloader:

.. code-block:: php

	require 'vendor/autoload.php';
