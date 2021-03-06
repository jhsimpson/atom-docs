.. _dc-template:

==================================================
Dublin Core Metadata Element Set, Version 1.1 (DC)
==================================================

.. note::

   A more fulsome description of AtoM's Dublin Core template including EAD and
   CSV import mappings will be made available soon.

On this page you will find:

* Link to downloadable CSV template using
  `ISAD(G) General International Standard Archival Description <http://www.ica.org/10207/standards/isadg-general-international-standard-archival-description-second-edition.html>`_
* Description of fields used when entering or importing
  :term:`archival descriptions <archival description>` using DC
  in a :term:`CSV` file or entering the data manually.

.. seealso::

   * :ref:`archival-descriptions`
   * :ref:`csv-testing-import`
   * :ref:`import-descriptions-terms`
   * :ref:`export-descriptions-terms`

.. _dc-and-csv:

Dublin Core and the ISAD CSV template
=====================================

At present, there is no DC-based CSV template for importing descriptions
into  AtoM. However, because is based on the `International Council
on Archives <http://www.ica.org/>`_ ' ISAD(G) standard (see:
:ref:`ISAD <isad-template>`), the ISAD CSV template
can be used for import, as all templates have been crosswalked in AtoM where
possible.

To test this, we recommend creating a full DC description in AtoM, and then
changing the display template to DC, to determine where field in DC map to
ISAD. For more information on changing the display template for a description,
see: :ref:`change-display-standard`. If desired, all templates in AtoM can be
changed at the  same time using the *Default template* setting available in
**Admin > Settings** - see :ref:`default-templates`.

The CSV mappings below will provide guidance on which ISAD CSV fields can be
used to import your DC-based descriptions into AtoM.

To download the ISAD(G) CSV template for AtoM, please visit our wiki page
(link to come).

Field descriptions
==================

AtoM implements unqualified
`Dublin Core Metadata Element Set, Version 1.1 <http://dublincore.org/documents/dces/>`_,
which is maintained by the `Dublin Core Metadata Initiative <http://dublincore.org>`__.

Information below includes:

* **Template field** refers to the default label for that field in AtoM
* **CSV Column** refers to the title of the related column in the (ISAD) CSV
  template
* **DC Rule** refers to the rule from the applicable standard and/or the
  instructions provided by AtoM.
* **DC XML** refers to the field mapping to MODS XML for import/export
* **Notes** includes any other information needed for successful data entry or
  CSV import.

**Skip to**:

* :ref:`dc-elements-area`

.. _dc-elements-area:

DC Elements area
================

.. figure:: images/dc-elements-area.*
   :align: center
   :figwidth: 50%
   :width: 100%
   :alt: An image of the data entry fields in the DC elements.

   The data entry fields for the Dublin Core archival description edit template.

Identifier
----------

In Dublin Core, an identifier is "an unambiguous reference to the resource
within a given context. Recommended best practice is to identify the resource
by means of a string conforming to a formal identification system."


Title
-----

"A name given to the resource. Typically, a Title will be a name by which the
resource is formally known."


Names and dates
---------------

Name(s)
^^^^^^^

In the "Actor name" field enter the first few letters of the the actor's name.
A list of names will appear in the drop-down menu (generated from the names of
existing authority records). If the name does not appear in the menu, type the
name and a new authority record will be created.

You can leave the "Actor name" field blank. Lower levels inherit creator
information from higher levels: use only if the creator is different at the
lower and higher levels. At the highest level of description, you should
always include the creator.

Select the type of event from the drop-down menu: creation, contribution or
publication. The value list is drawn from the event types taxonomy and can be
edited by system administrators and editors.

Date(s)
^^^^^^^

In Dublin Core 1.1, The date field corresponds to a "date associated with an
event in the life cycle of the resource. Typically, Date will be associated
with the creation or availability of the resource."

If desired, enter the date range as you want it to appear in view mode in "Date".
Add any additional text to qualify date range (e.g. "ca. 1940-1980" or
"[1940]-1980, predominant 1973-1980").

Enter the Start and End dates. Do not use any qualifiers here
(e.g. "ca.") or typographical symbols (e.g. "[194?]") to express uncertainty.
If the start and end years are the same, enter data only in the "Start" field and
leave the "End date" blank.

Complete at lower levels of description even if you are leaving the creator
name field blank (e.g. when describing a series, you do not need to repeat the
creator name from the fonds description, but you do need to enter the date
range of the series).

Whereas "Start" and "End" are used internally for database searching and
sorting purposes, this field is for display purposes. However, if you do not
enter anything into "Date" the "Start" and "End date" will appear as a
date range when the record is saved.

Subject
--------

"The topic of the resource. Typically, the subject will be represented using
keywords, key phrases, or classification codes. Recommended best practice is
to use a controlled vocabulary. To describe the spatial or temporal topic of
the resource, use the Coverage element."

Click on the "Subject" field and enter the first few letters of the term.
If the subject term does not appear on the list, type it in and a new subject
term will be created.

.. IMPORTANT::

   If you are not careful, it is easy to accidentally create duplicate terms!
   To avoid duplication, matching terms **must** be selected from the
   auto-complete :term:`drop-down <drop-down menu>` - otherwise, even exact
   matches will create duplicates when the user presses enter.

You can add multiple subjects, as desired. As you exit the :term:`field`, AtoM
will automatically add a new field below. If you wish to remove an access point,
hover your cursor over the bullet point next to the term - it will transform into
an "**X**". You can click the **X** to remove the term.

.. SEEALSO::

   * :ref:`terms`
   * :ref:`add-term-fly`

Description
-----------

"An account of the resource. Description may include but is not limited to: an
abstract, a table of contents, a graphical representation, or a free-text
account of the resource."

.. NOTE::

   This element will map to Scope and Content in equivalent archival standards
   such as :ref:`RAD <rad-template>`, :ref:`DACS <dacs-template>`, and
   :ref:`ISAD(G) <isad-template>`.

Type
----

The nature or genre of the resource. Recommended best practice is to use a
controlled vocabulary such as the DCMI Type Vocabulary [DCMITYPE]. To
describe the file format, physical medium, or dimensions of the resource, use
the Format element." For more information on the Dublin Core type taxonomy,
see http://dublincore.org/documents/dcmi-type-vocabulary/.

Select a value from the drop-down menu. The values are drawn from the "Dublin
Core Types" :term:`taxonomy`. AtoM comes with the DCMI TYPE terms prepopulated
in the taxonomy.

Child levels
------------

These two fields can be used to add lower levels to a collection level
description. Click "Add new" to create as many child levels as necessary.


**Identifier:** The unambiguous reference code used to uniquely identify the
child-level resource.

**Title:** The name given to the child-level resource.

Format
------

"The file format, physical medium, or dimensions of the resource. Examples of
dimensions include size and duration. Format may be used to determine the
software, hardware or other equipment needed to display or operate the
resource.Recommended best practice is to use a controlled vocabulary such as
the list of Internet Media Types [MIME]."

.. IMPORTANT::

   If the resource you are currently describing is already linked to
   a digital object, the Internet Media Types (MIME) will be added automatically
   upon output. It is recommended that you avoid duplicating those values here.

Source
------

"A related resource from which the described resource is derived. The
described resource may be derived from the related resource in whole or in
part." Recommended best practice is to identify the related resource by means
of a string conforming to a formal identification system.

Language
--------

"A language of the resource. Recommended best practice is to use a controlled
vocabulary such as RFC 4646."

Click on the field and the first few letters of the language. You can do this
as many times as you like to enter multiple languages.


Relation (isLocatedAt)
----------------------

This field is used for indicating which :term:`archival institution` holds the
record(s) being described. Select an archival institution only at the highest
:term:`level of description`; leave this field blank at the lower levels if
they are all held by the same institution.

.. TIP::

   To improve the description workflow and to respect the convention in most
   archival standards not to repeat information at lower levels, AtoM will
   inherit the name of the :term:`repository` from the highest level of
   description, unless a different repository is explicitly added.

Click on the Relation (isLocatedAt) field and type the first few letters of
the archival institution that holds the archival material being described. The
names are drawn from pre-existing archival institution records. If the name of
the institution does not appear in this list, you can type it in and a new
archival institution record will be created.

.. IMPORTANT::

   If you are not careful, it is easy to accidentally create duplicate
   repositories! To avoid duplication, matching terms **must** be selected from
   the auto-complete :term:`drop-down <drop-down menu>` - otherwise, even exact
   matches will create duplicates when the user presses enter.

.. SEEALSO::

   * :ref:`archival-institutions`
   * :ref:`link-archival-institution`

Coverage
--------

"The spatial or temporal topic of the resource, the spatial applicability of
the resource, or the jurisdiction under which the resource is relevant."

Click on the "Coverage (spatial)" field and type the first few letters of the
place. If the place term does not appear on the list, type it in and a new
place term will be created (note that this works only if you have taxonomy
edit permission).

Rights
------

"Information about rights held in and over the resource. Typically, rights
information includes a statement about various property rights associated
with the resource, including intellectual property rights."

For more information on using the fields contained in this dialog, see
:ref:`Add/edit rights <rights>`.


:ref:`Back to the top <dc-template>`
