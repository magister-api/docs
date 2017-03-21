=============
Configuration
=============


Introduction
============

All of the configuration files for the Magister 6 API are stored in the config directory. Feel free to look through the files and get familiar with the options available to you.


Environment Configuration
=========================

The Magister 6 API stores the configuration in the environment. It is often helpful to have different configuration values based on the environment the application is running in. There are two ways of modifying the Magister 6 API's configuration, one utilizing a third party package and one utilizing native PHP. Both of these ways serve the same purpose, although in a different way.


Using the DotEnv PHP library
----------------------------

The DotEnv PHP library by Vance Lucas uses a .env file to load environment variables to the PHP environment. You will need to add this package to your Composer requirements. Once this is done, simply create a ``.env`` file in your root directory and define your configuration options in there. See the `.env.example` file provided by the Magister 6 API for a sample configuration.

You need to instantiate the Dotenv class before creating a Magister instance:

.. code-block:: php

    $dotenv = new Dotenv\Dotenv(__DIR__);
    $dotenv->load();

    $magister = new Magister\Magister(...);

For more information on how to use phpdotenv, visit their `GitHub <https://github.com/vlucas/phpdotenv>`_ page. 


Using native PHP
----------------

Although the DotEnv PHP library is our preferred method, the same is possible without using any third party packages while sticking to native PHP functions. We need to use the following function to create an environment variable:

.. code-block:: php

    putenv("FOO=BAR");

This will set the environment variable ``FOO`` to the value ``BAR``. This does the exact same as the phpdotenv package, although instead of in a ``.env`` file, the environment variables are defined directly in your code. Likewise, these need to be defined before you create the Magister object. You can imagine this becoming a mess when you need to define multiple environment variables like this.


Retrieving Environment Configuration
------------------------------------

All of the configuration variables defined will be loaded into the ``$_ENV`` PHP super-global when your application receives a request. The Magister 6 API uses an ``env`` helper to retrieve values from these variables in the configuration files. 

.. code-block:: php

    'key' => env('MAGISTER_ENCRYPTION_KEY', null),

The second value passed to the ``env`` function is the "default value". This value will be used if no environment variable exists for the given key.

By default all Magister configuration options are prefixed by ``MAGISTER_``.
