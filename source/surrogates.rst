==========
Surrogates
==========


Introduction
============

Surrogates provide a "static" interface to classes that are available in the application's service container. The Magister 6 API ships with many surrogates which provide access to almost all of the Magister 6 API's features. The Magister 6 API's surrogates serve as "static proxies" to underlying classes in the service container, providing the benefit of a terse, expressive syntax while maintaining more testability and flexibility than traditional static methods.

All of the Magister 6 API's surrogates are defined in the ``Magister\Services\Support\Surrogates`` namespace. So, we can easily access a surrogate like so:

.. code-block:: php

    use Magister\Services\Support\Surrogates\Config;

    echo Config::get('app.key');

Throughout the Magister 6 API's documentation, many of the examples will use surrogates to demonstrate various features of the API.


Surrogate Class Reference
=========================

Below you will find every surrogate and its underlying class. This is a useful tool for quickly digging into the API documentation for a given surrogate root. The service container binding key is also included where applicable.

+--------+-----------------------------------------+---------------------------+
| Facade | Class                                   | Service Container Binding |
+========+=========================================+===========================+
| App    | Magister\Magister                       | ``app``                   |
+--------+-----------------------------------------+---------------------------+
| Auth   | Magister\Services\Auth\AuthManager      | ``auth``                  |
+--------+-----------------------------------------+---------------------------+
| Config | Magister\Services\Config\Repository     | ``config``                |
+--------+-----------------------------------------+---------------------------+
| Cookie | Magister\Services\Cookie\CookieJar      | ``cookie``                |
+--------+-----------------------------------------+---------------------------+
| Crypt  | Magister\Services\Encryption\Encrypter  | ``encrypter``             |
+--------+-----------------------------------------+---------------------------+
| Event  | Magister\Services\Events\Dispatcher     | ``events``                |
+--------+-----------------------------------------+---------------------------+
| File   | Magister\Services\Filesystem\Filesystem | ``files``                 |
+--------+-----------------------------------------+---------------------------+
| Http   | GuzzleHttp\Client                       | ``http``                  |
+--------+-----------------------------------------+---------------------------+
