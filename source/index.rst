Magister 6 API Documentation
============================

Welcome to the documentation for our public Magister 6 API. This project aims to provide an easy-to-use and elegant bridge between your website and Magister 6.

Please note that we are not affiliated with SchoolMaster's Magister in any way.

.. code-block:: php

    // Set the encryption key.
    putenv("MAGISTER_ENCRYPTION_KEY=$key");

    // Instantiate the Magister object.
    new Magister\Magister($school, $username, $password);

    // Display today's appointments.
    foreach (Magister\Models\Appointment::today() as $appointment) {
        // Display the description of the appointment.
        echo $appointment->Omschrijving;
    }

User Guide
==========

.. toctree::
   :maxdepth: 3
   
   installation
   configuration
