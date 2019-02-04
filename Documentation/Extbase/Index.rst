
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

exttables.sql
===================
Here added the table-structure. Using 9.5 LTS I dont need to configure system-fields like uid, hodde, startdate etc. or PROMARY KEY.

.. code-block:: php

    #
    # Table structure for table 'tx_events_domain_model_eventlocation'
    #
    CREATE TABLE tx_events_domain_model_eventlocation (
        title varchar(255) DEFAULT '' NOT NULL,
    );

    #
    # Table structure for table 'tx_events_domain_model_event'
    #
    CREATE TABLE tx_events_domain_model_event (
        title varchar(255) DEFAULT '' NOT NULL,
        subheadline varchar(255) DEFAULT '' NOT NULL,
        teaser text,
        description text,
        images int(11) DEFAULT '0' NOT NULL,
        files int(11) DEFAULT '0' NOT NULL,
        link varchar(255) DEFAULT '' NOT NULL,
        startdate int(11) unsigned DEFAULT '0' NOT NULL,
        enddate int(11) unsigned DEFAULT '0' NOT NULL,
        eventtype int(11) DEFAULT '0' NOT NULL,
        eventlocation int(11) DEFAULT '0' NOT NULL,
    );

event.php (parent model)
===================

Here I need to add the field and the getter-/setter.methods for the connection to the child

.. code-block:: php

    /**
     * eventlocation
     *
     * @var \TYPO3\CMS\Extbase\Persistence\ObjectStorage<\SvenWiener\Events\Domain\Model\Eventlocation>
     * @cascade remove
     * @lazy
     */
    protected $eventlocation = '';

    /**
     * Get Eventlocation
     *
     * @return \TYPO3\CMS\Extbase\Persistence\ObjectStorage
     */
    public function getEventlocation()
    {
        return $this->eventlocation;
    }

    /**
     * Set Eventlocation
     *
     * @param \TYPO3\CMS\Extbase\Persistence\ObjectStorage $eventlocation
     * @return void
     */
    public function setEventlocation($eventlocation)
    {
        $this->eventlocation = $eventlocation;
    }








