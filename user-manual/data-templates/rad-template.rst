.. _rad-template:

================================================================
Rules for Archival Description (RAD) data entry and CSV template
================================================================

On this page you will find:

* Link to downloadable CSV template using
  `Rules for Archival Description <http://www.cdncouncilarchives.ca/archdesrules.html>`_
* Description of fields used when entering or importing
  :term:`archival descriptions <archival description>` using Rules for Archival
  Description in a :term:`CSV` file or entering the data manually.

.. seealso::

   * :ref:`archival-descriptions`
   * :ref:`csv-testing-import`


RAD CSV template
================

To download the Rules for Archival Description CSV template for AtoM 2.0,
please visit our wiki page (link to come).

Field descriptions
==================

RAD is maintained by the `Canadian Council of Archives
<http://www.cdncouncilarchives.ca>`_ and is available at
http://www.cdncouncilarchives.ca/archdesrules.html.

Information below includes:

* **Template field** refers to the default label for that field in AtoM
* **CSV Column** refers to the title of the column in the CSV template
* **RAD Rule** refers to the rule from the applicable standard and/or the
  instructions provided by AtoM.
* **EAD** refers to the field mapping to EAD
* **Notes** includes any other information needed for successful data entry or
  CSV import.

**Skip to**:

* :ref:`Title and statement of responsibility area <template-title>`
* :ref:`Edition area <template-edition>`
* :ref:`Class of material specific details area <template-class>`
* :ref:`Authority record fields <template-authority>`
* :ref:`Dates of creation area <template-dates>`
* :ref:`Physical description area <template-physical>`
* :ref:`Publisher's series area <template-publishers>`
* :ref:`Archival description area <template-description>`
* :ref:`Notes area <template-notes>`
* :ref:`Standard number area <template-standard-number>`
* :ref:`Access points <template-access>`
* :ref:`Control area <template-control>`
* :ref:`Rights area <template-rights>`
* :ref:`Administration area <template-admin>`

.. _template-title:

Title and statement of responsibility area
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. figure:: images/title-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Title and statement of
         responsibility area

   The data entry fields for Title proper, GMD, Parallel titles, Other title
   information, and Statement of responsibility

Title proper
------------

**Template field** Title proper

**CSV Column** title

**RAD Rule** Enter the title proper, either transcribed or supplied (RAD 1.1B)

**EAD**

At a parent level:

.. code:: bash

   <archdesc level="[name of level]">
      <did>
         <unittitle encodinganalog="1.1B">

At a child level:

.. code:: bash

   <c level="[name of level]>
      <did>
         <unittitle encodinganalog="1.1B">

.. note::

   The EAD tag ``<titleproper encodinganalog="title">`` refers to the
   title of the finding aid, not the archival description.

:ref:`Back to the top <rad-template>`

General material designation
----------------------------

**Template field** General material designation

**CSV Column** radGeneralMaterialDesignation

**RAD Rule** Select the General Material Designation at the highest level of
description. If there are more than three, select "multiple media." (RAD 1.1C)

**EAD**

.. code:: bash

   <archdesc>
      <controlaccess>
         <genreform encodinganalog="1.1C">

.. note::

   Although the RAD standard specifies set values for General Material
   Designations, in AtoM these can be edited in the Material type
   :term:`taxonomy` (see: :ref:`Add a new term <add-term>`). If you try to
   import a CSV file using a different :term:`term` from the taxonomy, the
   import will fail. See
   `Bug 6567 <https://projects.artefactual.com/issues/6757>`_ .


:ref:`Back to the top <rad-template>`

Parallel title
--------------

**Template field** Parallel title

**CSV Column** alternateTitle

**RAD Rule** [W]hen applicable, transcribe parallel titles that appear in
conjunction with the formal title proper...(RAD 1.1D)

**EAD**

.. code:: bash

   <archdesc level="[name of level]" relatedencoding="RAD">
      <did>
         <unittitle type="parallel" encodinganalog="1.1D">


:ref:`Back to the top <rad-template>`

Other title information
-----------------------

**Template field** Other title information

**CSV Column** radOtherTitleInformation

**RAD Rule** Transcribe other title information that appears in conjunction with
the formal title proper. (RAD 1.1E)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle type="otherInfo" encodinganalog="1.1E">

:ref:`Back to the top <rad-template>`

Title statement of responsibility
---------------------------------

**Template field** Statements of responsibility

**CSV Column** radTitleStatementOfResponsibility

**RAD Rule** "At the item level of description, transcribe explicit statements of
responsibility appearing in conjunction with the formal title proper in or on
the chief source of information..." (RAD 1.1F)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle type="statRep">

:ref:`Back to the top <rad-template>`

.. figure:: images/title-notes.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Title notes area

   The data entry fields for Title notes. Multiple title notes can be added
   by clicking "Add new."

Title notes- Statements of responsibility
-----------------------------------------

**Template field** Title notes- Statements of responsibility

**CSV Column** radTitleStatementOfResponsibilityNote

**RAD Rule** "Make notes on any statement(s) of
responsibility that appear outside the chief source of information or that appear on the
chief source, but not in conjunction with a formal title proper. Record statements of
responsibility that appear on the chief source of information for a file or series, if
applicable." (RAD 1.8B5)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="titleStatRep">

:ref:`Back to the top <rad-template>`

Title notes- Attributions and conjectures
-----------------------------------------

**Template field** Title notes- Attributions and conjectures

**CSV Column** radTitleAttributionsAndConjectures

**RAD Rule** "Make notes on authors to whom the unit being
described has been attributed, and cite sources, if appropriate." (RAD 1.8B6)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="titleAttributions">

:ref:`Back to the top <rad-template>`

Title notes- Continuation of title
----------------------------------

**Template field** Title notes- Continuation of title

**CSV Column** radTitleContinues

**RAD Rule** "Complete the transcription if the formal title proper and/or
other title information was abridged in the description." (RAD 1.8B4)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="titleContinuation">

:ref:`Back to the top <rad-template>`

Title notes- Source of title proper
-----------------------------------

**Template field** Title notes- Source of title proper

**CSV Column** radTitleSourceOfTitleProper

**RAD Rule** "Indicate the source of a title proper, when appropriate." (RAD
1.8B2)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="titleSource">

:ref:`Back to the top <rad-template>`

Title notes- Variations in title
--------------------------------

**Template field** Title notes- Variations in title

**CSV Column** radTitleVariationsInTitle

**RAD Rule** "Make notes on variant titles appearing outside the prescribed
source of information. Make notes on titles by which the unit being described has been
traditionally known other than the title proper." (RAD 1.8B1)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="titleVariation">

:ref:`Back to the top <rad-template>`

Title notes- Parallel titles and other title information
--------------------------------------------------------

**Template field** Title notes- Parallel titles and other title information

**CSV Column** radTitleParallelTitles

**RAD Rule** "Make notes on parallel titles and other title information not
recorded in the Title and statement of responsibility area if they are
considered to be important." (RAD 1.8B3)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="titleParallel">

:ref:`Back to the top <rad-template>`

.. figure:: images/title-area-2.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Level of description, new
         child levels, Repository and Identifier.

   The data entry fields for Level of description, child levels, Repository
   and Identifier. Multiple child levels can be added by clicking "Add new."

Level of description
--------------------

**Template field** Level of description

**CSV Column** levelOfDescription

**RAD Rule** Select a level of description from the drop-down menu. See RAD 1.0A for
rules and conventions on selecting levels of description.

**EAD**


At the parent level:

.. code:: bash

   <archdesc level="fonds" relatedencoding="RAD">


At the child level:

.. code:: bash

   <dsc type="combined>
      <c level="[name of level]">

.. note::

   An :term:`administrator` can edit the values in the Levels of
   description :term:`taxonomy` (see: :ref:`Add a new term <add-term>`). In
   CSV import, if a term is used that is not already in the taxonomy, it will
   be added to the Levels of description taxonomy.

:ref:`Back to the top <rad-template>`

Add new child levels
--------------------

.. image:: images/add-new-child-widget.*
   :align: center
   :width: 80%
   :alt: Add new child widget in RAD

**Template field** Identifier, Level, Title, Date

**CSV Column** See notes below

**RAD Rule** *Identifier*: Enter an unambiguous code used to uniquely identify the
description.

*Level*: Select a level of description from the drop-down menu.
See RAD 1.0A for rules and conventions on selecting levels of description.

*Title*: Enter the title proper, either transcribed or supplied (RAD 1.1B).

*Date*: (Works similarly to the display date field when adding a date of
creation; see :ref:` below <template-dates>` for more information in RAD)

**EAD** N/A

.. note::

   This widget has been added to help improve workflows when creating new
   descriptions via the :term:`user interface`.  When entering descriptions
   manually, users can add new :term:`child records <child record>` in this area
   while creating a parent record.

   The *dates* field corresponds to a date of creation - if you would like a
   different kind of date, you will have to either navigate to the child
   description after saving the new :term:`parent record`, and change the date
   type, or simply ignore the date field in the widget, and add the correct
   date type manually to the child record after saving the new parent record.

   In CSV import, adding child records can be achieved using the *legacyID* and
   *parentID* columns. See :ref:`csv-legacy-id-mapping`.

Repository
----------

**Template field** Repository

**CSV Column** repository

**RAD Rule** Select the repository that has custody and
control of the archival material. The values in this field are drawn from the
Authorized form of name field in archival institution records. Search for an
existing name by typing the first few characters of the name. Alternatively,
type a new name to create and link to a new archival institution.

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <repository>
            <corpname>

:ref:`Back to the top <rad-template>`

Reference code
--------------

**Template field** Identifier

**CSV Column** identifier

**RAD Rule** Enter an unambiguous code used to uniquely identify the description.

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unitid encodinganalog="1.8B11">

.. note::

   This field displays to non-logged in users as "Reference code."
   While editing the record, the full reference code including any identifiers
   :ref:`inherited <inherit-reference-code>` from higher levels will appear
   below the Identifier field.


:ref:`Back to the top <rad-template>`

Alternative identifier
----------------------

**Template field** Add alternative identifier(s) [link beneath identifier
field]

**CSV Column** Not currently available in AtoM CSV import

**RAD Rule** N/A (see note below)

**EAD**

.. code:: bash

   <archdesc level="[name of level]">
      <did>
         <unitid type="alternative" label="[user entered value]">

.. note::

   The use of the alternative identifier fields is documented in full here:

   * :ref:`add-alternative-id`


:ref:`Back to the top <rad-template>`


.. _template-edition:

Edition area
^^^^^^^^^^^^
.. figure:: images/edition-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Edition area.

   The data entry fields for the Edition area.

Edition statement
-----------------

**Template field** Edition statement

**CSV Column** radEdition

**RAD Rule** "Transcribe the edition statement relating to the item being
described." (RAD 1.2B1) "If the item being described lacks an edition
statement but is known to contain significant changes from other editions,
supply a suitable brief statement in the language and script of the title
proper and enclose it in square brackets." (RAD 1.2B3)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle encodinganalog="1.2B1">
            <edition>

.. note::

   This field also maps to the ``<editionstmt><edition>`` tag in
   ``<eadheader><filedesc>``.

:ref:`Back to the top <rad-template>`

Edition statement of responsibility
-----------------------------------

**Template field** Edition statement of responsibility

**CSV Column** radEditionStatementOfResponsibility

**RAD Rule** "Transcribe a statement of responsibility relating to one or more
editions, but not to all editions, of the item being described following the
edition statement if there is one." (RAD 1.2.C1) "When describing the first
edition, give all statements of responsibility in the Title and statement of
responsibility area." (RAD 1.2C2)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle type="statRep" encodinganalog="1.2C">
            <edition>

:ref:`Back to the top <rad-template>`

.. _template-class:

Class of materials specific details area
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. figure:: images/class-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Class of materials specific
         details area.

   The data entry fields for the Class of materials specific details area.


RAD: "1.3A. Preliminary rule: 1.3A1. Scope: For instructions regarding this
area, refer to the chapters dealing with the class(es) of material that use
it."


Statement of scale (cartographic)
---------------------------------

**Template field** Statement of scale (cartographic)

**CSV Column** radStatementOfScaleCartographic

**RAD Rule** "Give the scale of the unit being described...as a representative
fraction (RF) expressed as a ratio (1: ). Precede the ratio by Scale. Give the
scale even if it is already recorded as part of the title proper or other
title information." (RAD 5.3B1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <materialspec type="cartographic" encodinganalog="5.3B1">

:ref:`Back to the top <rad-template>`

Statement of projection (cartographic)
--------------------------------------

**Template field** Statement of projection (cartographic)

**CSV Column** radStatementOfProjection

**RAD Rule** "Give the statement of projection if it is found on the prescribed
source(s) of information." (RAD 5.3C1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <materialspec type="projection" encodinganalog="5.3C1">

:ref:`Back to the top <rad-template>`

Statement of coordinates (cartographic)
---------------------------------------

**Template field** Statement of coordinates (cartographic)

**CSV Column** radStatementOfCoordinates

**RAD Rule** "At the fonds, series or file levels, record coordinates for the
maximum coverage provided by the materials in the unit, as long as they are
reasonably contiguous." (RAD 5.3D)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <materialspec type="coordinates" encodinganalog="5.3D">

:ref:`Back to the top <rad-template>`

Statement of scale (architectural)
----------------------------------

**Template field** Statement of scale (architectural)

**CSV Column** radStatementOfScaleArchitectural

**RAD Rule** "Give in English the scale in the units of measure found on the unit
being described. If there is no English equivalent for the name of the unit
of measure, give the name, within quotation marks, as found on the unit
being described." (RAD 6.3B)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <materialspec type="architectural" encodinganalog="6.3B">

:ref:`Back to the top <rad-template>`

Issuing jurisdiction and denomination (philatelic)
--------------------------------------------------

**Template field** Issuing jurisdiction and denomination (philatelic)

**CSV Column** radIssuingJurisdiction

**RAD Rule** "Give the name of the jurisdiction (e.g., government) responsible for
issuing the philatelic records." (RAD 12.3B1) "For all units possessing a
denomination (e.g., postage stamps, revenue stamps, postal stationery items),
give the denomination in a standardized format, recording the denomination
number in arabic numerals followed by the name of the currency unit. Include a
denomination statement even if the denomination is already recorded as part of
the title proper or other title information." (RAD 12.3C1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <materialspec type="philatelic" encodinganalog="12.3B1">

:ref:`Back to the top <rad-template>`

.. _template-authority:

Authority record fields
^^^^^^^^^^^^^^^^^^^^^^^

These fields are found in the CSV template but when entering descriptions
manually are found in the :term:`authority record`. However, the description can be
linked to the authority record while entering the data manually.

Creator
-------

**Template field** Creator

**CSV Column** creators

**RAD Rule** Use the Actor name field to link an authority record to this
description. Search for an existing name in the authority records by typing
the first few characters of the name. Alternatively, type a new name to
create and link to a new authority record.

**EAD**

.. code:: bash

   <archdesc>
      <bioghist encodinganalog="1.7B">
         <chronlist>
            <chronitem>
               <eventgrp>
                  <event>
                     <origination encodinganalog="1.7C">
                        <name>

.. NOTE::

   This is the default export EAD when an Entity type has not been set for the
   actor on the related :term:`authority record`. The final EAD element can be
   more precise, if the user has entered an Entity type on the related
   :term:`authority record`. When the Entity type is set to **Person**, the EAD
   will export using ``<persname>`` instead of  ``<name>``; when set to
   **Family**, the EAD will export using ``<famname>``  instead of ``<name>``;
   and when set to **Organization**, the EAD will export using ``<corpname>``
   instead of ``<name>``. The ``<name>`` element is the default when no
   entity type is set. For more information on authority records and the ISAAR
   standard upon which the authority record template is based, see:
   :ref:`authority-records` and :ref:`isaar-template`.

.. TIP::

   When entering the description manually, the Creator field is found in the
   RAD template  within the Dates of creation :term:` information area`,
   labeled as "Actor name."

:ref:`Back to the top <rad-template>`

Biographical history
--------------------

**Template field** Biographical history

**CSV Column** creatorHistories

**RAD Rule** "Record in narrative form or as a chronology the main life events,
activities, achievements and/or roles of the entity being described. This may
include information on gender, nationality, family and religious or political
affiliations. Wherever possible, supply dates as an integral component of the
narrative description." (ISAAR 5.2.2)

See also RAD section 1.7B1.

**EAD**

.. code:: bash

   <archdesc>
      <bioghist encodinganalog="1.7B">
         <chronlist>
            <chronitem>
               <eventgrp>
                  <event>
                     <note>


.. note::

   When entering data manually, this field needs to be written in the
   :term:`authority record`. If an authority record does not already exist, AtoM
   will create one when a new creator is entered, above. The user can then
   navigate to the authority record to enter the Biographical or Administrative
   history (see: :ref:`Authority records <authority-records>`).

When importing descriptions by CSV, by default this column will
create a Biographical history in the :term:`authority record`, regardless of
whether the creator is a person, family, or organization. To specify the
entity type when importing creators, users would need to
:ref:`import authority records <csv-import-authority-records>`.

:ref:`Back to the top <rad-template>`

.. _template-dates:

Dates of creation area
^^^^^^^^^^^^^^^^^^^^^^

When entering data manually, the fields below are accessed by clicking "Add
new" in the dates of creation area.

.. figure:: images/event-entry.*
   :align: right
   :figwidth: 35%
   :width: 100%
   :alt: An image of the data entry fields for the Dates of Creation area

   The data entry fields for the Dates of Creation area

Entering an actor's name will automatically insert the actor's
biographical sketch or administrative history from the
:term:`authority record`.

When entering data manually, users can choose an event type from a
:term:`drop-down menu`. The event types can be edited by an
:term:`administrator` in the Event types :term:`taxonomy` (see:
:ref:`Add a new term <add-term>`). When importing descriptions via CSV, the
event type defaults to Creation.

Place
-----

**Template field** Place

**CSV Column** N/A

**RAD Rule** "For an item, transcribe the place of publication, distribution,
etc., in the form and grammatical case in which it appears." (RAD 1.4C1).
Search for an existing term in the places taxonomy by typing the first few
characters of the term name. Alternatively, type a new term to create and
link to a new place term.

**EAD** N/A

.. note::

   This field does not map to EAD due to its relation to a specific
   event.

Date(s)
-------

**Template field** Date(s)

**CSV Column** creatorDates

**RAD Rule** "Give the date(s) of creation of the unit being described either as a
single date, or range of dates (for inclusive dates and/or predominant dates).
Always give the inclusive dates. When providing predominant dates, specify
them as such, preceded by the word predominant..." (1.4B2). Record probable
and uncertain dates in square brackets, using the conventions described in RAD
1.4B5.

**EAD**

.. code:: bash

   <archdesc>
      <bioghist encodinganalog="1.7B">
         <chronlist>
            <chronitem>
               <date type="creation">

.. note::

   This field will display the date as intended by the editor of the
   archival description, in the language of the standard being used.

:ref:`Back to the top <rad-template>`

Dates of creation- Start
------------------------

**Template field** Dates of creation- Start

**CSV Column** creatorDatesStart

**RAD Rule** Enter the start year. Do not use any qualifiers or typographical
symbols to express uncertainty. Acceptable date formats: YYYYMMDD,
YYYY-MM-DD, YYYY-MM, YYYY.

**EAD**

.. code:: bash

   <archdesc>
      <bioghist encodinganalog="1.7B">
         <chronlist>
            <chronitem>
               <date type="creation" normal="[start/end]">

.. note::

   This field only displays while editing the description. If AtoM is
   able to interpret the start date from the Date(s) field, above, it will
   autopopulate upon entering.

:ref:`Back to the top <rad-template>`

Dates of creation- End
----------------------

**Template field** Dates of creation- End

**CSV Column** creatorDatesEnd

**RAD Rule** Enter the end year. Do not use any qualifiers or typographical symbols
to express uncertainty. Acceptable date formats: YYYYMMDD,
YYYY-MM-DD, YYYY-MM, YYYY.

**EAD**

.. code:: bash

   <archdesc>
      <bioghist encodinganalog="1.7B">
         <chronlist>
            <chronitem>
               <date type="creation" normal="[start/end]">
.. note::

   This field only displays while editing the description. If AtoM is
   able to interpret the start date from the Date(s) field, above, it will
   autopopulate upon entering.

:ref:`Back to the top <rad-template>`

Dates of creation- Note
-----------------------

**Template field** Dates of creation- Note

**CSV Column** creatorDatesNotes

**RAD Rule** "Make notes on dates and any details pertaining to the dates of
creation, publication, or distribution, of the unit being described that are
not included in the Date(s) of creation, including publication, distribution,
etc., area and that are considered to be important. " (RAD 1.8B8) "Make notes
on the date(s) of accumulation or collection of the unit being described." RAD
1.8B8a)

**EAD**

.. code:: bash

   <archdesc>
      <bioghist encodinganalog="1.7B">
         <chronlist>
            <chronitem>
               <eventgrp>
                  <event>
                     <note type="eventNote">

.. note::

   This appears while editing as "Event note."

:ref:`Back to the top <rad-template>`

.. _template-physical:

Physical description area
^^^^^^^^^^^^^^^^^^^^^^^^^

.. figure:: images/physical-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Physical description area.

   The data entry fields for the Physical description area.


Physical description
--------------------

**Template field** Physical description

**CSV Column** extentAndMedium

**RAD Rule** "At all levels record the extent of the unit being described by
giving the number of physical units in arabic numerals and the specific
material designation as instructed in subrule .5B in the chapter(s) dealing
with the broad class(es) of material to which the unit being described
belongs." (RAD 1.5B1) Include other physical details and dimensions as
specified in RAD 1.5C and 1.5D. Separate multiple entries in this field with a
carriage return (i.e. press the Enter key on your keyboard).

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <physdesc>
            <extent encodinganalog="1.5B1">


:ref:`Back to the top <rad-template>`

.. _template-publishers:

Publisher's series area
^^^^^^^^^^^^^^^^^^^^^^^

.. figure:: images/publishers-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Publisher's series area.

   The data entry fields for the Publisher's series area.

Title proper of publisher's series
----------------------------------

**Template field** Title proper of publisher's series

**CSV Column** radTitleProperOfPublishersSeries

**RAD Rule** "At the item level of description, transcribe a title proper of the
publisher's series as instructed in 1.1B1." (RAD 1.6B)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle>
            <bibseries>
               <title encodinganalog="1.6B1">


:ref:`Back to the top <rad-template>`

Parallel titles of publisher's series
-------------------------------------

**Template field** Parallel titles of publisher's series

**CSV Column** radParallelTitlesOfPublishersSeries

**RAD Rule** "Transcribe parallel titles of a publisher's series as instructed in
1.1D." (RAD 1.6C1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle>
            <bibseries>
               <title type="parallel" encodinganalog="1.6C1">


:ref:`Back to the top <rad-template>`

Other title information of publisher's series
---------------------------------------------

**Template field** Other title information of publisher's series

**CSV Column** radOtherTitleInformationOfPublishersSeries

**RAD Rule** "Transcribe other title information of a publisher's series as
instructed in 1.1E and only if considered necessary for identifying the
publisher's series." (RAD 1.6D1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle>
            <bibseries>
               <title type="otherInfo" encodinganalog="1.6D1">


:ref:`Back to the top <rad-template>`


Statement of responsibility relating to publisher's series
----------------------------------------------------------

**Template field** Statement of responsibility relating to publisher's series

**CSV Column** radStatementOfResponsibilityRelatingToPublishersSeries

**RAD Rule** "Transcribe explicit statements of responsibility appearing in
conjunction with a formal title proper of a publisher's series as instructed
in 1.1F and only if considered necessary for identifying the publisher's
series." (RAD 1.6E1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle>
            <bibseries>
               <title type="statRep" encodinganalog="1.6E1">

:ref:`Back to the top <rad-template>`


Numbering within publisher's series
-----------------------------------

**Template field** Numbering within publisher's series

**CSV Column** radNumberingWithinPublishersSeries

**RAD Rule** "Give the numbering of the item within a publisher's series in the
terms given in the item." (RAD 1.6F1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unittitle>
            <bibseries>
               <num encodinganalog="1.6F">


:ref:`Back to the top <rad-template>`

Note on publisher's series
--------------------------

**Template field** Note on publisher's series

**CSV Column** radPublishersSeriesNote

**RAD Rule** "Make notes on important details of publisher's series that are not
included in the Publisher's series area, including variant series titles,
incomplete series, and of numbers or letters that imply a series." (RAD
1.8B10)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="bibSeries">

.. note::

   This field maps to the same EAD field as the field in Notes area below,
   Other notes- Publisher's Series. Both notes refer to RAD 1.8B10.

:ref:`Back to the top <rad-template>`

.. _template-description:

Archival description area
^^^^^^^^^^^^^^^^^^^^^^^^^

.. figure:: images/archival-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Archival description area.

   The data entry fields for the Archival description area.

Custodial history
-----------------

**Template field** Custodial history

**CSV Column** archivalHistory

**RAD Rule** "Give the history of the custody of the unit being described, i.e., the
successive transfers of ownership and custody or control of the material,
along with the dates thereof, insofar as it can be ascertained." (RAD 1.7C)

**EAD**

.. code:: bash

   <archdesc>
      <custodhist encodinganalog="1.7C">


:ref:`Back to the top <rad-template>`

Scope and content
-----------------

**Template field** Scope and content

**CSV Column** scopeAndContent

**RAD Rule** "At the fonds, series, and collection levels of description, and when
necessary at the file and the item levels of description, indicate the level
being described and give information about the scope and the internal
structure of or arrangement of the records, and about their contents." (RAD
1.7D)

"For the scope of the unit being described, give information about the
functions and/or kinds of activities generating the records, the period of
time, the subject matter, and the geographical area to which they pertain.
For the content of the unit being described, give information about its
internal structure by indicating its arrangement, organization, and/or
enumerating its next lowest level of description. Summarize the principal
documentary forms (e.g., reports, minutes, correspondence, drawings,
speeches)." (RAD 1.7D1)

**EAD**

.. code:: bash

   <archdesc>
      <scopecontent encodinganalog="1.7D">


:ref:`Back to the top <rad-template>`

.. _template-notes:

Notes area
^^^^^^^^^^

.. figure:: images/notes-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the notes area.

   The data entry fields for the Notes area. More notes fields continue below
   the screen shown.

Physical condition
------------------

**Template field** Physical condition

**CSV Column** physicalCharacteristics

**RAD Rule** "Make notes on the physical condition of the unit being described if
that condition materially affects the clarity or legibility of the records."
(RAD 1.8B9a)

**EAD**

.. code:: bash

   <archdesc>
      <phystech encodinganalog="1.8B9a">

:ref:`Back to the top <rad-template>`

Immediate source of acquisition
-------------------------------

**Template field** Immediate source of acquisition

**CSV Column** acquisition

**RAD Rule** "Record the donor or source (i.e., the immediate prior custodian) from
whom the unit being described was acquired, and the date and method of
acquisition, as well as the source/donor's relationship to the material, if
any or all of this information is not confidential. If the source/donor is
unknown, record that information." (RAD 1.8B12)

**EAD**

.. code:: bash

   <archdesc>
      <acqinfo encodinganalog="1.8B12">

:ref:`Back to the top <rad-template>`

Arrangement
-----------

**Template field** Arrangement

**CSV Column** arrangement

**RAD Rule** "Make notes on the arrangement of the unit being described which
contribute significantly to its understanding but cannot be put in the Scope
and content (see 1.7D), e.g., about reorganisation(s) by the creator,
arrangement by the archivist, changes in the classification scheme, or
reconstitution of original order." (RAD 1.8B13)

**EAD**

.. code:: bash

   <archdesc>
      <arrangement encodinganalog="1.8B13">

:ref:`Back to the top <rad-template>`

Language of material
--------------------

**Template field** Language of material

**CSV Column** language

**RAD Rule** "Record the language or languages of the unit being described, unless
they are noted elsewhere or are apparent from other elements of the
description." RAD (1.8.B14).

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <langmaterial encodinganalog="1.8B9a">
            <language langcode="___">

.. note::

   Use a three-letter language code from
   `ISO 639-2 <http://www.loc.gov/standards/iso639-2/php/code_list.php>`_ when
   importing from CSV.

:ref:`Back to the top <rad-template>`

Script of material
------------------

**Template field** Script of material

**CSV Column** script

**RAD Rule** "[N]ote any distinctive alphabets or symbol systems employed."
RAD (1.8.B14)

**EAD** <langmaterial> <language scriptcode>

.. code:: bash

   <archdesc>
      <did>
         <langmaterial encodinganalog="1.8B9a">
            <language scriptcode="___">

.. note::

   Use a three-letter language code from
   `ISO 639-2 <http://www.loc.gov/standards/iso639-2/php/code_list.php>`_ when
   importing from CSV.

:ref:`Back to the top <rad-template>`


Language and script note
------------------------

**Template field** Language and script note

**CSV Column** languageNote

**RAD Rule** "Record the language or languages of the unit being described, unless
they are noted elsewhere or are apparent from other elements of the
description. Also note any distinctive alphabets or symbol systems employed."
RAD (1.8.B14).

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <langmaterial encodinganalog="1.8B9a">

.. note::

   Not intended to duplicate information from language or script, above.

:ref:`Back to the top <rad-template>`


Location of originals
---------------------

**Template field** Location of originals

**CSV Column** locationOfOriginals

**RAD Rule** "If the unit being described is a reproduction and the location of the
original material is known, give that location. Give, in addition, any
identifying numbers that may help in locating the original material in the
cited location. If the originals are known to be no longer extant, give that
information." (RAD 1.8B15a)

**EAD**

.. code:: bash

   <archdesc>
      <originalsloc encodinganalog="1.8B15a">

:ref:`Back to the top <rad-template>`


Availability of other formats
-----------------------------

**Template field** Availability of other formats

**CSV Column** locationOfCopies

**RAD Rule** "If all or part of the unit being described is available (either in the
institution or elsewhere) in another format(s), e.g., if the text being
described is also available on microfilm; or if a film is also available on
videocassette, make a note indicating the other format(s) in which the unit
being described is available and its location, if that information is known.
If only a part of the unit being described is available in another
format(s), indicate which parts." (RAD 1.8B15b)

**EAD**

.. code:: bash

   <archdesc>
      <altformavail encodinganalog="1.8B15b">

:ref:`Back to the top <rad-template>`


Restrictions on access
----------------------

**Template field** Restrictions on access

**CSV Column** accessConditions

**RAD Rule** "Give information about any restrictions placed on access to the unit
(or parts of the unit) being described." (RAD 1.8B16a)

**EAD**

.. code:: bash

   <archdesc>
      <accessrestrict encodinganalog="1.8B16a">


:ref:`Back to the top <rad-template>`

Terms governing use, reproduction, and publication
--------------------------------------------------

**Template field** Terms governing use, reproduction, and publication

**CSV Column** reproductionConditions

**RAD Rule** "Give information on legal or donor restrictions that may affect use or
reproduction of the material." (RAD 1.8B16c)

**EAD**

.. code:: bash

   <archdesc>
      <userestrict encodinganalog="1.8B16c">

:ref:`Back to the top <rad-template>`


Finding aids
------------

**Template field** Finding aids

**CSV Column** findingAids

**RAD Rule** "Give information regarding the existence of any finding aids. Include
appropriate administrative and/or intellectual control tools over the
material in existence at the time the unit is described, such as card
catalogues, box lists, series lists, inventories, indexes, etc." (RAD
1.8B17)

**EAD**

.. code:: bash

   <archdesc>
      <otherfindaid encodinganalog="1.8B17">

:ref:`Back to the top <rad-template>`

Associated materials
--------------------

**Template field** Associated materials

**CSV Column** relatedUnitsOfDescription

**RAD Rule** For associated material, "If records in another institution are
associated with the unit being described by virtue of the fact that they
share the same provenance, make a citation to the associated material at the
fonds, series or collection level, or for discrete items, indicating its
location if known." (RAD 1.8B18).

For related material, "Indicate groups of records having some significant
relationship by reason of shared responsibility or shared sphere of activity
in one or more units of material external to the unit being described." (RAD
1.8B20).

**EAD**

.. code:: bash

   <archdesc>
      <relatedmaterial encodinganalog="1.8B18">

:ref:`Back to the top <rad-template>`


Accruals
--------

**Template field** Accruals

**CSV Column** accruals

**RAD Rule** "When the unit being described is not yet complete, e.g., an open fonds
or series, make a note explaining that further accruals are expected... If
no further accruals are expected, indicate that the unit is considered
closed." (RAD 1.8B19)

**EAD**

.. code:: bash

   <archdesc>
      <accruals encodinganalog="1.8B19">

:ref:`Back to the top <rad-template>`

.. figure:: images/notes-other.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the other notes fields.

   The data entry fields for Other notes. Multiple notes can be added by
   clicking "Add new"

Other notes- Accompanying material
----------------------------------

**Template field** Other notes- Accompanying material

**CSV Column** radNoteAccompanyingMaterial

**RAD Rule** "Give details of accompanying material not mentioned
in the Physical description area (see 1.5E)." (RAD 1.8B9c)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="material" encodinganalog="1.5E">

:ref:`Back to the top <rad-template>`



Other notes- Alpha-numeric designations
---------------------------------------

**Template field** Other notes- Alpha-numeric designations

**CSV Column** radNoteAlphaNumericDesignation

**RAD Rule** "If desirable, make a note of any important
numbers borne by the unit being described other than publisher's series numbers (see
1.6F) or standard numbers (see 1.9)." (RAD 1.8 B11)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="alphanumericDesignation">

:ref:`Back to the top <rad-template>`

Other notes- Cast note
----------------------

**Template field** Other notes- Cast note

**CSV Column** radNoteCast

**RAD Rule** "List featured players, performers, presenters or other on-screen
personnel." (Moving images - RAD 7.8B5b)

**EAD**

.. NOTE::

   At this time, the RAD Cast note field in AtoM has not been mapped to the EAD
   import/export.

:ref:`Back to the top <rad-template>`


Other notes- Conservation
-------------------------

**Template field** Other notes- Conservation

**CSV Column** radNoteConservation

**RAD Rule** "If the unit being described has received any specific
conservation treatment, e.g., if repair work has been done on it, briefly indicate the
nature of the work." (RAD 1.8B9b)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="conservation" encodinganalog="1.8B9b">

:ref:`Back to the top <rad-template>`

Other notes- Credits note
-------------------------

**Template field** Other notes- Credits note

**CSV Column** radNoteCredits

**RAD Rule** "List persons (other than the cast) who have contributed to the
artistic and/or technical production of a moving image document. Preface each
name or group of names with a statement of function." (Moving images - RAD
7.8B5a)

**EAD**

.. NOTE::

   At this time, the RAD Credits note field in AtoM has not been mapped to the
   EAD import/export.

:ref:`Back to the top <rad-template>`

Other notes- Edition
--------------------

**Template field** Other notes- Edition

**CSV Column** radNoteEdition

**RAD Rule** "Make notes relating to the edition being described or of the relationship
of the unit being described to other editions." (RAD 1.8B7)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="edition" encodinganalog="1.8B7">

:ref:`Back to the top <rad-template>`


Other notes- Physical description
---------------------------------

**Template field** Other notes- Physical description

**CSV Column** radNotePhysicalDescription

**RAD Rule** "Make notes relating to the physical description of the unit
being described." (RAD 1.8B9)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="physDesc">

:ref:`Back to the top <rad-template>`


Other notes- Publisher's series
-------------------------------

**Template field** Other notes- Publisher's series

**CSV Column** radPublishersSeriesNote

**RAD Rule** "Make notes on important details of publisher's series that are not
included in the Publisher's series area, including variant series titles,
incomplete series, and of numbers or letters that imply a series." (RAD
1.8B10)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="bibSeries">

.. note::

   This column maps to the same EAD field as the column above,
   Note on Publishers Series. Both notes refer to RAD 1.8B10.

:ref:`Back to the top <rad-template>`


Other notes- Rights
-------------------

**Template field** Other notes- Rights

**CSV Column** radNoteRights

**RAD Rule** "Indicate the copyright status, literary rights, patents or any
other rights pertaining to the unit being described." (RAD 1.8B16b)

**EAD**

.. code:: bash

   <archdesc>
      <odd type="rights" encodinganalog="1.8B16b">

:ref:`Back to the top <rad-template>`

Other notes- Signatures note
----------------------------

**Template field** Other notes- Signatures note

**CSV Column** radNoteSignatures

**RAD Rule** "Make notes on signatures, inscriptions, or monograms, etc.,
which appear on the unit being described. Indicate where such signatures and
inscriptions appear."(RAD 3.8B6)

*See also*: RAD 4.8B7 (Graphic materials); RAD 5.8B6 (Cartographic materials);
RAD 6.8B6 (Architecture and technical drawings); RAD 11.8B7 (Objects); and
RAD 12.8B7 (Philatelic records).

**EAD**

.. NOTE::

   At this time, the RAD Signatures note field in AtoM has not been mapped to
   the EAD import/export.

:ref:`Back to the top <rad-template>`

Other notes- General note
-------------------------

**Template field** Other notes- General note

**CSV Column** radNoteGeneral

**RAD Rule** "Use this note to record any other descriptive information
considered important but not falling within the definitions of the other notes.
(RAD 1.8B21).

**EAD**

.. code:: bash

   <archdesc>
      <odd type="general" encodinganalog="1.8B21">

:ref:`Back to the top <rad-template>`

.. _template-standard-number:

Standard number area
^^^^^^^^^^^^^^^^^^^^

.. figure:: images/standard-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Standard number area.

   The data entry fields for the Standard number area.

Standard number
---------------

**Template field** Standard number

**CSV Column** radStandardNumber

**RAD Rule** "Give the International Standard Book Number (ISBN), International
Standard Serial Number (ISSN), or any other internationally agreed standard
number for the item being described. Give such numbers with the agreed
abbreviation and with the standard spacing or hyphenation." (RAD 1.9B1)

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <unitid type="standard" encodinganalog="1.9B1">

:ref:`Back to the top <rad-template>`

.. _template-access:

Access points
^^^^^^^^^^^^^

.. figure:: images/access-points.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for Access points.

   The data entry fields for Access points.

Subject access points
---------------------

**Template field** Subject access points

**CSV Column** subjectAccessPoints

**RAD Rule** "Search for an existing term in the Subjects taxonomy by typing the
first few characters of the term. Alternatively, type a new term to create and
link to a new subject term."

**EAD**

.. code:: bash

   <archdesc>
      <controlaccess>
         <subject>

.. note::

   The values in this column/field will create
   :term:`terms <term>` in the subjects :term:`taxonomy` where those do not
   already exist.

:ref:`Back to the top <rad-template>`


Place access points
-------------------

**Template field** Place access points

**CSV Column** placeAccessPoints

**RAD Rule** "Search for an existing term in the Places taxonomy by typing the
first few characters of the term name. Alternatively, type a new term to
create and link to a new place term."

**EAD**

.. code:: bash

   <archdesc>
      <controlaccess>
         <geogname>

.. note::

   The values in this column/field will create :term:`terms <term>` in the
   places :term:`taxonomy` where those do not already exist.

:ref:`Back to the top <rad-template>`


Name access points
------------------

**Template field** Name access points

**CSV Column** nameAccessPoints

**RAD Rule** "Choose provenance, author and other non-subject access points from
the archival description, as appropriate. All access points must be apparent
from the archival description to which they relate." (RAD 21.0B) The values in
this field are drawn from the Authorized form of name field in authority
records. Search for an existing name by typing the first few characters of the
name. Alternatively, type a new name to create and link to a new authority
record.

**EAD**

If the entity type of the actor is not defined as either a person, family, or
corporate body:

.. code:: bash

   <archdesc>
      <controlaccess>
         <name role="subject">

For a personal name:

.. code:: bash

   <archdesc>
      <controlaccess>
         <persname role="subject">

For a family name:

.. code:: bash

   <archdesc>
      <controlaccess>
         <famname role="subject">

For a corporate body or organizational name:

.. code:: bash

   <archdesc>
      <controlaccess>
         <corpname role="subject">
.. note::

   The values in this column/field will create
   :term:`authority records <authority record>` where those do not already exist.

:ref:`Back to the top <rad-template>`

.. _template-control:

Control area
^^^^^^^^^^^^

.. figure:: images/control-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Control area.

   The data entry fields for the Control area. More fields continue below the
   screen shown.

For more information on the use of fields in the control area, see
:ref:`control area <control-area>`.


Description record identifier
-----------------------------

**Template field** Description record identifier

**CSV Column** descriptionIdentifier

**RAD Rule** "Record a unique description identifier in accordance with local
and/or national conventions. If the description is to be used
internationally, record the code of the country in which the description was
created in accordance with the latest version of ISO 3166- Codes for the
representation of names of countries. Where the creator of the description is
an international organisation, give the organisational identifier in place of
the country code."

**EAD**

.. code:: bash

   <archdesc>
      <odd type="descriptionIdentifier">

:ref:`Back to the top <rad-template>`


Institution identifier
----------------------

**Template field** Institution identifier

**CSV Column** institutionIdentifier

**RAD Rule** "Record the full, authorised form of name(s) of the agency(ies)
responsible for creating, modifying, or disseminating the description, or,
alternatively, record a code for the agency in accordance with the national
or international agency code standard."

**EAD**

.. code:: bash

   <archdesc>
      <odd type="institutionIdentifier">

:ref:`Back to the top <rad-template>`


Rules or conventions
--------------------

**Template field** Rules or conventions

**CSV Column** rules

**RAD Rule** "Record the international, national, and/or local rules or
conventions followed in preparing the description."

**EAD**

.. code:: bash

   <eadheader>
      <profiledesc>
         <descrules encodinganalog="3.7.2">

:ref:`Back to the top <rad-template>`


Status
------

**Template field** Status

**CSV Column** descriptionStatus

**RAD Rule** "Record the current status of the description, indicating whether it
is a draft, finalized, and/or revised or deleted."

**EAD**

.. code:: bash

   <archdesc>
      <odd type="statusDescription">

.. note::

   AtoM uses a :term:`taxonomy` to determine the value of this field.
   If you try to import a CSV file using a different :term:`term` from the
   taxonomy, the import will succeed, but a null value will be entered for
   Status (see `Bug 6758 <https://projects.artefactual.com/issues/6758>`_ . The
   default terms are Final, Revised and Draft, but can be edited through the
   :ref:`Manage taxonomy screen <add-term-taxonomy>`.

:ref:`Back to the top <rad-template>`


Level of detail
---------------

**Template field** Level of detail

**CSV Column** levelOfDetail

**RAD Rule** "Record whether the description consists of a minimal, partial, or
full level of detail in accordance with relevant international and/or
national guidelines and/or rules."

**EAD**

.. code:: bash

   <archdesc>
      <odd type="levelOfDetail">

.. note::

   AtoM uses a :term:`taxonomy` to determine the value of this field.
   If you try to import a CSV file using a different :term:`term` from the
   taxonomy, the import will fail (see
   `Bug 6756 <https://projects.artefactual.com/issues/6756>`_. The default terms
   are Full, Partial and Minimal, but can be edited through the
   :ref:`Manage taxonomy screen <add-term-taxonomy>`.

:ref:`Back to the top <rad-template>`


Dates of creation, revision and deletion
----------------------------------------

**Template field** Dates of creation, revision and deletion

**CSV Column** revisionHistory

**RAD Rule** "Record the date(s) the entry was prepared and/or revised."

**EAD**

.. code:: bash

   <archdesc>
      <processinfo>
         <date>


.. note::

   This is a free text field, allowing users to also write narrative
   notes about the revision history of the description.

:ref:`Back to the top <rad-template>`


Language of description
-----------------------

**Template field** Language of description

**CSV Column** languageOfDescription

**RAD Rule** "Indicate the language(s) used to create the description of the
archival material."

**EAD**

.. code:: bash

   <eadheader>
      <profiledesc>
         <language>
            <language langcode="___">

.. note::

   In CSV import, use a three-letter language code from
   `ISO 639-2 <http://www.loc.gov/standards/iso639-2/php/code_list.php>`_ .
   When entering data manually, AtoM will offer an autocomplete drop-down
   list as you type, which will be generated as a three-letter language code
   in the EAD.

:ref:`Back to the top <rad-template>`


Script of description
---------------------

**Template field** Script of description

**CSV Column** scriptOfDescription

**RAD Rule** "Indicate the script(s) used to create the description of the
archival material."

**EAD**

.. code:: bash

   <eadheader>
      <profiledesc>
         <language>
            <language scriptcode="____">

.. note::

   In CSV import, use a four-letter script code from
   `ISO 1924 <http://www.unicode.org/iso15924/iso15924-codes.html>`_. When
   entering data manually, AtoM will offer an autocomplete drop-down
   list as you type, which will be generated as a four-letter script code
   in the EAD.

:ref:`Back to the top <rad-template>`


Sources
-------

**Template field** Sources

**CSV Column** sources

**RAD Rule** "Record citations for any external sources used in the archival
description (such as the Scope and Content, Custodial History, or Notes
fields)."

**EAD**

.. code:: bash

   <archdesc>
      <did>
         <note type="sourcesDescription">

.. note::

   If there are sources to cite used used in a biographical
   sketch or administrative history, record these in the sources field for the
   :term:`authority record`.


:ref:`Back to the top <rad-template>`

.. _template-rights:

Rights area
^^^^^^^^^^^

.. figure:: images/rights-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the rights area.

   The data entry area for the Rights area. Multiple rights records can be
   added by clicking "Add new."

This area of the description allows users to enter a :term:`rights record`
compliant with `PREMIS <http://www.loc.gov/standards/premis/>`_. These fields
are separate from the RAD rights notes, above, and editing one area does not
effect the other. Rights records cannot be imported with descriptions via CSV.

For more information, see
:ref:`Add rights to an archival description <rights-archival-description>`.

.. _template-admin:

Administration area
^^^^^^^^^^^^^^^^^^^

.. figure:: images/admin-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields for the Administration area.

   The data entry fields for the Administration area.

Publication status
------------------

**Template field** Publication status

**CSV column** publicationsStatus

**RAD Rule** N/A

**EAD**

.. code:: bash

   <archdesc>
      <odd type="publicationStatus">

.. note::

   In the :ref:`Global Site Settings <global-settings>`, if the default
   publication status is set to draft, all imported descriptions will be set to
   draft and the EAD file will have the value "draft" in the
   <odd type="publicationStatus"> tag.

:ref:`Back to the top <rad-template>`

Display standard
----------------

**Template field** Display standard

**CSV column** N/A

**RAD Rule** N/A

**EAD** N/A

.. note::

   This fields allows the user to choose a different display standard
   from the :ref:`default template <default-templates>`
   for the shown archival description only, with the option to also change the
   display standard for all existing children of the description.


:ref:`Back to the top <rad-template>`

Appraisal
---------

**Template field** N/A

**CSV Column** Appraisal

**RAD Rule** N/A

**EAD**

.. code:: bash

   <archdesc>
      <appraisal encodinganalog="3.3.2">

.. note::

   There is no appraisal field in Rules for Archival Description and
   therefore this field does not display in the AtoM RAD template. However,
   contents of this column are contained in the EAD file and can be
   exported/imported.

:ref:`Back to the top <rad-template>`

