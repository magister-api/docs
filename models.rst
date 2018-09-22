======
Models
======


A model is the interface between the API and your code. Each model has a set of default methods and optional model specific methods.


Grade
=====

Clearly, this model can be used to retrieve information about grades. After creating a instance of the Magister class, a model can be used by first including the corresponding namespace:


.. code-block:: php

    use Magister\Models\Grade\Grade;
    
Retrieving all grades
---------------------
Since the Magister API utilizes surrogates, each model can be treated as a static class. For example, if one whishes to retrieve all grades, one can simply do:

.. code-block:: php
    
    $grades = Grade::all();
    
Retrieving the first grade
--------------------------
The first grade can be retrieved by doing:

.. code-block:: php

    $grade = Grade::first();
    
Request parameters
------------------
At some models, the user can specify parameters. This can be done with the :php:`where()` function. For example:

.. code-block:: php
    
    $grades = Grade::where('actievePerioden', 'false')->get();
