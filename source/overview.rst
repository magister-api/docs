========
Overview
========


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

	php composer.phar require stanvk/magister-api:~2.0

Alternatively, you can specify the Magister 6 API as a dependency in your project's existing composer.json file:

.. code-block:: js

	{
	   "require": {
	      "stanvk/magister": "~2.0"
	   }
	}

Make sure you run the Composer install command after modifying your composer.json file in order to update your vendor folder.

After installing, you need to require Composer's autoloader:

.. code-block:: php

	require 'vendor/autoload.php';

You can find out more on how to install Composer, configure autoloading, and other best-practices for defining dependencies at `getcomposer.org <http://getcomposer.org>`_.


License
=======

The Magister 6 API is licensed using the `MIT license <http://opensource.org/licenses/MIT>`_.

	Copyright (c) 2015 Stanvk & KickWood

	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the "Software"), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is
	furnished to do so, subject to the following conditions:

	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
	SOFTWARE.


Contributing
============

Guidelines
----------

1. The Magister 6 API utilizes the `PSR-2 <https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md>`_ coding standard and the `PSR-4 <https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md>`_ autoloading standard.
2. The Magister 6 API is meant to be lean and fast with very few dependencies. This means
   that not every feature request will be accepted.
3. The Magister 6 API has a minimum PHP version requirement of PHP 5.4. Pull requests must
   not require a PHP version greater than PHP 5.4 unless the feature is only
   utilized conditionally.