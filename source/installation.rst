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

    php composer.phar require stanvk/magister:~2.0

Alternatively, you can specify the Magister 6 API as a dependency in your project's existing composer.json file:

.. code-block:: js

    {
       "require": {
          "stanvk/magister": "~2.0"
       }
    }

Make sure you run the ``php composer.phar install`` command after modifying your composer.json file in order to update your vendor directory.

After installing, you need to require Composer's autoloader:

.. code-block:: php

    require 'vendor/autoload.php';

You can find out more on how to install Composer, configure autoloading, and other best-practices for defining dependencies at `getcomposer.org <http://getcomposer.org>`_.


Configuration
=============

Configuration Files
-------------------

All of the configuration files for the Magister 6 API are stored in the config directory. Feel free to look through the files and get familiar with the options available to you.

Encryption Key
--------------

The next thing you should do after installing the Magister 6 API is set your encryption key to a random string. 

Typically, this string should be 32 characters long. The key can be set in your PHP environment. The Magister 6 API ships with a function to generate a secure encryption key. Use the following function to generate a 32 characters long secure encryption key:

.. code-block:: php

    str_random(32);

For more information on how to set the encryption key in your environment, visit the :doc:`configuration section </configuration>` of the documentation.

**If the encryption key is not set, your user sessions and other encrypted data will not be secure!**
