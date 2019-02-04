
.. include:: ../Includes.txt

=================
Extbase
=================

**Here you can find my hints an code examples for extension-development in extbase**

Relations between tables
----------------------

**There are several methods to realize realtions between tables. Here I give an overview after my experiences**

My extension (events) got the possibility to create child-objects (eventlocations) in the backend. So I added/extended these files in my extension-folder:

- exttables.sql
- Classes/Domain/Model/Event.php
- Classes/Domain/Model/Eventlocation.php
- Configuration/TCA/tx_events_domain_model_event.php
- Configuration/TCA/tx_events_domain_model_eventlocation.php
- Resources/Private/Language/locallang_db.xlf
- Resources/Public/Icons/tx_events_domain_model_eventlocation.gif

.. code-block:: php

   composer update











