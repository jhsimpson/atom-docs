.. _archival-descriptions:

=====================
Archival Descriptions
=====================

.. |plus| image:: images/plus-sign.png
   :height: 18
   :width: 18

Archival descriptions are one of the core :ref:`entity-types` in AtoM and
provide users with invaluable contextual infomation about the resources held
by an :term:`archival institution`.

In AtoM, an archival description is a body of information about an archival
record or records. The descriptions provide contextual information about the
archival materials and are arranged into hierarchical levels (:term:`fonds`,
series, files, items, and variations of these in accordance with institutional
standards).

Archival desription is *also* an activity, however - generally accompanied by
the process of archival arrangemenent, it is the outcome of a process to gain
intellectual control over a resource or collection of resources and provide
end users (such as :term:`researchers <researcher>`) with a means of
conceptualizing the organization of these resources and navigating to the
specific content in which they are interested, as well as a sense of what is
contained, how it got there, and what role it serves in the larger
accumulation of materials. Archival description is therefore intended to
facilitate the identification, management, and understanding of archival
materials.

The International Council on Archives (`ICA <http://www.ica.org/>`__) defines
an archival description as *"The creation of an accurate representation of a
unit of description and its component parts, if any, by capturing, analyzing,
organizing and recording information that serves to identify, manage, locate
and explain archival materials and the context and records systems which
produced it. This term also describes the products of the process"* (ISAD
glossary).

Archival description is somewhat similar to the process of bibliographic
description, and some standards, such as the Canadian Rules for Archival
Description (RAD), are derived from bibliographic standards. Daniel Pitti,
one of the original creators of the Encoded Archival Description XML-based
metadata exchange standard (`EAD <http://www.loc.gov/ead/>`__), points out that
one of the key differences, however, is in the hierarchical nature of
archival description:

    *The distinction between what and for whom libraries and archives remember
    accounts form the major differences in archival and bibliographic
    description. A bibliographic description, such as that found in a MARC
    record, represents an individual published item, and thus is item-level.
    There is a one-to-one correspondence between the description and the item.
    The description is based on, and is derived from, the physical item.
    Archival description represents a fonds, a complex body of materials,
    frequently in more than one form or medium, sharing a common provenance.
    The description involves a complex hierarchical and progressive analysis.
    It begins by describing the whole, then proceeds to identify and describe
    sub-components of the whole, and sub-components of sub-components, and so
    on. Frequently, but by no means always, the description terminates with a
    description of individual items. The description emphasizes the
    intellectual structure and content of the material, rather than their
    physical characteristics.* (`Pitti, 1999
    <http://www.dlib.org/dlib/november99/11pitti.html>`__)

Archival description is often preceded by the creation of an :ref:`accession
record <accession-records>`, and much of the information generated during the
accessions process can be re-used to create archival descriptions. As new
:term:`accruals <accrual>` are added, the archival description is updated to
reflect these changes.

.. TIP::

   AtoM can generate an :term:`archival description` from an existing
   :term:`accession record` - see :ref:`Create an archival description from an
   accession record <create-accession-description>` for more information.

.. image:: images/arch-desc.*
   :align: center
   :width: 80%
   :alt: Example of an archival description in AtoM

**Below are instructions for using the Archival description module in AtoM
to:**

* :ref:`Add a new archival description <add-archival-description>`

  * :ref:`Add a new child description <add-child-archival-description>`

* :ref:`Edit an existing archival description <edit-archival-description>`

  * :ref:`Publish an archival description <publish-archival-description>`

* :ref:`Duplicate an existing archival description
  <duplicate-archival-description>`
* :ref:`link-related-descriptions`
* :ref:`change-display-standard`
* :ref:`add-alternative-id`
* :ref:`Move an archival description <move-archival-description>`
* :ref:`Delete an archival description <delete-archival-description>`

AtoM also includes standards-based templates for describing resources. Please
see the sections below for more specific instructions on the use of
:term:`fields  <field>` within each template:

* General International Standard Archival Description:
  :ref:`ISAD(G) <isad-template>`
* Describing Archives: A Content Standard (U.S.A): :ref:`DACS <dacs-template>`
* Dublin Core Metadata Element Set, Version 1.1: :ref:`Dublin Core <dc-template>`
* Metadata Object Description Schema: :ref:`MODS <mods-template>`
* Rules for Archival Description (Canada): :ref:`RAD <rad-template>`

.. seealso::

   * :ref:`add-term-fly`
   * :ref:`Physical storage <link-physical-storage>`
   * :ref:`Upload digital objects <upload-digital-object>`
   * :ref:`Create an archival description from an accession record
     <create-accession-description>`
   * :ref:`Link an accession record to an archival description
     <link-accession-description>`
   * :ref:`Exit edit mode <exit-edit-mode>`
   * :ref:`link-function-description`
   * :ref:`link-authority-to-description`
   * :ref:`upload-digital-object`
   * :ref:`rights-archival-description`
   * :ref:`import-descriptions-terms`
   * :ref:`csv-import`


.. _add-archival-description:

Add a new archival description
==============================

This section contains instructions on how to Add a new top level archival
description (also known as a :term:`parent record`), and how to add a new
child description (or :term:`child record`) via two different methods

.. _add-top-level-description:

Add a new top level description
-------------------------------

A new :term:`archival description` can be added at any time, from anywhere in
the application, via the :term:`main menu` available to authenticated (i.e.
logged in) AtoM users with the appropriate privileges (such as
:term:`contributors <contributor>`, :term:`editors <editor>`, and
:term:`administrators <administrator>`). For more information on User roles
and types of users in AtoM see: :ref:`User roles <user-roles>`.

.. NOTE::

   You must be logged in to be able to create a new :term:`archival
   description` in AtoM. See: :ref:`Log in <log-in>`.

**To create a new archival description:**

1. In the :term:`main menu` located in the :term:`header bar`, click the
   |plus| ":ref:`Add <main-menu-add>`" menu and select "Archival description"
   from the :term:`drop-down menu`.

.. image:: images/add-description.*
   :align: center
   :width: 30%
   :alt: An image of the Add menu in AtoM

2. AtoM takes you to a blank :term:`edit page` for data entry.

.. NOTE::

   The :term:`edit page` that appears will depend on the :ref:`default template
   <default-templates>` set in the application. When first installed, the
   default template in AtoM is the :ref:`ISAD(G) <isad-template>` (General
   International Standard for Archival Description) template. Administrators
   can change the default template to any of the other 4 supported standards
   (:ref:`RAD <rad-template>`, :ref:`DACS <dacs-template>`, :ref:`Dublin Core
   <dc-template>`, or :ref:`MODS <mods-template>` via **Admin >
   Settings > Default template**. For more information, see: :ref:`settings`.

3. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on an
   :term:`information area` to access the :term:`fields <field>` grouped under
   it. Enter data as required.

.. image:: images/description-collapsed.*
   :align: center
   :width: 85%
   :alt: An archival description with all information areas closed

4. Note that new lower :term:`levels of description <level of description>`
   (i.e. :term:`children <child record>`) can be created on the fly without
   leaving the top-level or :term:`parent <parent record>` description you are
   currently creating. For more information, see below, :ref:`Add a new child
   description <method-1-child-description>`.

.. image:: images/description-add-children.*
   :align: center
   :width: 85%
   :alt: An image of the add new children feature in an edit template

5. You can quit the create process at any time by clicking the "Cancel" button
   in the :term:`button block`; any data already entered will not be saved,
   and no new record will be created. Note that simply navigating away from
   the page by any other means, **without first clicking "Create"** will also
   result in no new record being created.
6. To save the new record, click the :term:`"Create" button <create button>`
   located in the :term:`button block` at the bottom of the record.

.. image:: images/button-block-create.*
   :align: center
   :width: 85%
   :alt: An image of the create button on a new archival description

.. NOTE::

   The default status of a newly created :term:`archival description` is
   DRAFT. :term:`Draft records <draft record>` are not visible to
   unauthenticated (i.e. not logged in) users such as :term:`researchers
   <researcher>`. Under the :term:`Administration area` of the archival
   description, users with publication privileges (see: :ref:`User roles
   <user-roles>`) can select :term:`PUBLISHED <published record>` as the new
   status of the archival description, making it available for read access to
   the public.

.. TIP::

   :term:`Administrators <administrator>` can also change the default
   publication status of new records throughout the application via **Admin >
   Settings > Global > Default publication status**. For more information,
   see: :doc:`Settings <../administer/settings>`.

:ref:`Back to top <archival-descriptions>`


.. _add-child-archival-description:

Add a new child description
---------------------------

A :term:`child descriptions <child record>` is an archival description that is
part of a larger hierarchy, often a :term:`fonds` or :term:`collection`. A
child record refers to a description of the :term:`archival unit` that is one
:term:`level of description` lower than the current unit - for example, if a
series belongs to a :term:`fonds`, the series is the child record of the
fonds. AtoM helps users understand the context of the materials by depicting
the current record's position in the :term:`treeview`, which can also be used
for navigation  (see: :doc:`Context menu <../access-content/context-menu>`)

There are two ways to add a new :term:`child description <child record>` in
AtoM - **Method 1** allows a user to add a new child record "on the fly" while
creating a top-level description (or :term:`parent record`), but these records
should be considered stubs or placeholders until they can be returned to and
supplemented with further description. **Method 2** explains how to create a
full child description at any time.

.. _method-1-child-description:

Method 1: "On the fly"
^^^^^^^^^^^^^^^^^^^^^^

AtoM includes a data entry element in the first :term:`information area` of
the :term:`archival description` :term:`edit page` that allows users to
generate lower :term:`levels of description <level of description>` to a
:term:`parent record` without leaving the current :term:`edit page`.

This area is located in:

* The **Identity** :term:`area <information area>` of the :ref:`ISAD(G)
  <isad-template>`  and :ref:`DACS <dacs-template>` templates
* The **Statement of responsibility** :term:`area <information area>` of the
  :ref:`RAD <rad-template>` template
* The **Elements** :term:`area <information area>` of the :ref:`Dublin Core
  <dc-template>`  and :ref:`MODS <mods-template>` templates

Note that this method is not meant to replace more granular description - it
allows a user to create a sort of skeleton structure to the whole of the
description (such as a :term:`fonds` or :term:`collection`), which can
improve supplement an archival :term:`arrangement` workflow - the :term:`child
<child record>` descriptions can then be supplemented later.

.. image:: images/description-add-children.*
   :align: center
   :width: 85%
   :alt: An image of the add new children feature in an edit template

:term:`Fields <field>` provided for creating lower levels of description "on
the fly" via the :term:`parent description's <parent record>` :term:`edit page`
include:

* Identifier (i.e., reference number)
* Level (of description)
* Title

.. TIP::

   You can add as many levels as needed at one time; for example, to add
   multiple series to a :term:`fonds` or :term:`collection`, fill in the fields
   under the "Add new child levels" and add as many lower levels as desired.
   When the record is saved, you will be able to see the new :term:`child
   records <child record>` in the :term:`context menu`.

.. _method-2-child-description:

Method 2: Adding a full child description
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Full :term:`child descriptions <child record>` can be added to an
:term:`archival description` at any time (by users with sufficient :ref:`edit
privileges <edit-user-permissions>`) by navigating to the description to which
you would like to add a child (the :term:`parent description <parent record>`).

First, navigate to the :term:`parent archival description <parent record>` to
which you wish to add a child description. You can do this by
:ref:`browsing <browse>` or :ref:`searching <search-atom>` for the
:term:`archival description` - see :ref:`Access content <access-content>`
for more information on navigation in AtoM.

.. NOTE::

   You must be logged in to be able to create a new :term:`archival
   description` in AtoM. See: :ref:`Log in <log-in>`.

1. In the :term:`view page` of the parent :term:`archival description`, scoll
   to the bottom of the record to the :term:`button block` and click the "Add
   new" button.

.. image:: images/button-block-description.*
   :align: center
   :width: 85%
   :alt: An image of the button block on an archival description view page

2. You will be redirected to a new :term:`archival description` :term:`edit page`.
   On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on an
   :term:`information area` to access the :term:`fields <field>` grouped under
   it. Enter data as required.

.. image:: images/description-collapsed.*
   :align: center
   :width: 85%
   :alt: An archival description with all information areas closed

.. IMPORTANT::

   It is important to note that after clicking on the "Add new" record button,
   the edit archival description template will appear, but no reference is
   made to the :term:`parent <parent record>` archival description. When you
   save your record, however, you will be able to see the relationship
   expressed in the :term:`treeview`, located in the :term:`context menu`
   on the left-hand side of the :term:`view page`.

3. Enter appropriate information into the template for the lower-level
   description, and remember to select the :term:`level of description`.
4. Note that you can add further :term:`children <child record>` to this lower
   level of description as you work, via The :ref:`"On the fly"
   <method-1-child-description>` method described above.

.. image:: images/description-add-children.*
   :align: center
   :width: 85%
   :alt: An image of the add new children feature in an edit template

5. You can quit the create process at any time by clicking the "Cancel" button
   in the :term:`button block`; any data already entered will not be saved,
   and no new child record will be created. Note that simply navigating away
   from the page by any other means, **without first clicking "Create"** will
   also result in no new record being created.
6. To save the new child record, click the :term:`"Create" button <create
   button>` located in the :term:`button block` at the bottom of the record.

.. image:: images/button-block-create.*
   :align: center
   :width: 85%
   :alt: An image of the create button on a new archival description

After clicking "Save" you will be redirected to the :term:`view page` for the
new child description. You can see the relationship to the parent record
expressed in the :ref:` context menu <context-menu>`. For more information on
the Context menu and the treeview in AtoM, see: :ref:`context-menu`, and
specifically, :ref:`context-menu-treeview`. See also: :ref:`treeview-search`.

:ref:`Back to top <archival-descriptions>`

.. _edit-archival-description:

Edit an existing archival description
=====================================

An authenticated (i.e. logged in) user with edit privileges can edit or update
an :term:`archival description` at any time. For more information on edit
privileges and user roles see: :ref:`User roles <user-roles>`. For information
on logging in, see: :ref:`Log in <log-in>`.

**To edit an existing archival description:**

1. First, navigate to the :term:`archival description` you wish to edit. You
   can do this by :ref:`browsing <browse>` or :ref:`searching <search-atom>`
   for the :term:`archival description` - see :ref:`access-content` for more
   information on navigation in AtoM.
2. Switch from :term:`view mode` to :term:`edit mode` by clicking the
   :term:`"Edit" button <Edit button>` in the :term:`button block`, or by
   clicking on one of the :term:`information area` headings; this takes you
   to the record's :term:`edit page`.
3. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on an
   information area to access the :term:`fields <field>` grouped under it. If
   you've clicked on an an :term:`area header` directly, the edit page will
   load with that area open.

.. image:: images/description-collapsed.*
   :align: center
   :width: 85%
   :alt: An archival description with all information areas closed

4. Add and/or revise data as required.
5. You can quit the create process at any time by clicking the "Cancel" button
   in the :term:`button block`; any changes made will not be saved. Note that
   simply navigating away from the page by any other means, **without first
   clicking "Save"** will also result in no changes being saved to the
   archival description.
6. To save your edits, click the "Save" button located in the :term:`button
   block` at the bottom of the record.

.. image:: images/button-block-save.*
   :align: center
   :width: 85%
   :alt: An image of the button block

You will be redirected to the :term:`view page` for the edited
:term:`archival description`, where you can review your work.


.. _publish-archival-description:

Publish an archival description
-------------------------------

All new and imported :term:`archival descriptions <archival description>` in
AtoM are automatically saved as :term:`draft records <draft record>`. This
means that users who are not authenticated (i.e. logged in) cannot view these
records.

.. NOTE::

   Administrators can change the default publication status, via **Admin >
   Settings**. For more information, see: :ref:`Settings <settings>`.

Publication status is inherited from the highest :term:`level of description`,
meaning that changes to the publication status of the :term:`parent record`
will affect the publication status of all :term:`child records <child
record>`. For example, when a :term:`fonds` description is changed from draft
to published, all child levels within the fonds (series, files, items, etc.)
are automatically changed as well.

If a :term:`contributor` (i.e. a logged in user **without** permission to
publish descriptions - see: :ref:`User roles <user-roles>`) edits a
:term:`published record`, the record's status is **automatically changed back
to draft**, unless the default publication status has been changed to *published*.

Changing a record's status to published allows unauthenticated users such as
:term:`researchers <researcher>` the ability to see the record, i.e. read
access is granted to the public. Draft records are not viewable by
unauthenticated users (i.e. those not logged in).


**To publish an existing archival description**

1. Navigate to the record you wish to publish. For more information on
   navigation in AtoM, see: :ref:`Access content <access-content>`
2. Switch from :term:`view mode` to :term:`edit mode` by clicking "Edit"
   button in the :term:`button block`, or by clicking on one of the
   :term:`information area` headings; this takes you to the record's
   :term:`edit page`.

.. image:: images/button-block-description.*
   :align: center
   :width: 85%
   :alt: An image of the button block on an archival description view page

3. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on the
   :term:`Administration area` heading to expand it and make changes.

.. image:: images/description-collapsed.*
   :align: center
   :width: 85%
   :alt: An archival description with all information areas closed

4. In the :term:`drop-down menu` underneath the subheading "Publication
   status", select "published".

.. image:: images/description-admin-area.*
   :align: center
   :width: 85%
   :alt: The Administration area in an archival description

5. Scroll down to the :term:`button block` at the bottom of the :term:`edit
   page` and click the "Save" button.

.. image:: images/button-block-save.*
   :align: center
   :width: 85%
   :alt: An image of the button block

The archival description, and any lower :term:`levels of description <level of
description>` associated with it, will now be published - public users who are
not logged will now be granted read access to view (but not edit) the
record(s). The record(s) will also be discoverable to public users via
:ref:`browse` or :ref:`search-atom`

:ref:`Back to top <archival-descriptions>`


.. _duplicate-archival-description:

Duplicate an existing archival description
==========================================

To simplify the description workflow when working with many similar
descriptions (such as, in some cases, many items in a :term:`collection`),
AtoM includes the ability to generate a duplicate record from an existing
:term:`archival description`, and then edit it to make necessary changes.
This can allow a user to avoid unnecessarily repeating data entry.

.. note::

   When duplicating a parent record, lower (child) levels of description will
   NOT be duplicated.

**To duplicate an existing archival description:**

1. First, navigate to the :term:`archival description` you wish to edit. You
   can do this by :ref:`browsing <browse>` or :ref:`searching <search-atom>`
   for the :term:`archival description` - see :ref:`access-content` for more
   information on navigation in AtoM.
2. At the bottom of the archival description, click the "Duplicate" button
   located in the :term:`button block`.

.. image:: images/button-block-description.*
   :align: center
   :width: 85%
   :alt: An image of the button block on an archival description view page

3. You will be redirected to a new screen with an :term:`edit page` of an
   :term:`archival description` open.
4. The new edit page provides a warning at the top to indicate that it is a
   duplicated record.

.. image:: images/description-duplicate-warning.*
   :align: center
   :width: 85%
   :alt: An image of a duplicated archival description

5. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on an
   information area to access the :term:`fields <field>` grouped under it.
   You will note that these will be populated with the exact same data found
   in the original :term:`archival description` - you can now make any edits
   or revisions necessary.
6. You can quit the create process at any time by clicking the "Cancel" button
   in the :term:`button block`; no new record will be created. Note that
   simply navigating away from the page by any other means, **without first
   clicking "Create"** will also result in no new record being created.
7. To save the duplicate as a new record, click the "Save" button located in
   the :term:`button block` at the bottom of the record.

.. image:: images/button-block-save.*
   :align: center
   :width: 85%
   :alt: An image of the button block

.. IMPORTANT::

   If you are duplicating a :term:`child <child record>` of a :term:`parent
   record` (such as a series, file, or item), the duplicate description will
   automatically be created as a :term:`child <child record>` of the same
   parent :term:`archival description`. If you duplicate a top or
   :term:`parent <parent record>` :term:`level of description`, the new
   record will also be a top-level description with no parent.

   Records can be moved in AtoM as well - see below,
   :ref:`Move an archival description <move-archival-description>`


:ref:`Back to top <archival-descriptions>`

.. _link-related-descriptions:

Link related archival descriptions in AtoM to each other
========================================================

Many AtoM descriptive templates include a free text field, derived from the
related content standards (for more information, see:
:ref:`descriptive-standards` and :ref:`data-entry`) that will allow users to
describe allied or related materials:

+------------------+----------+------------------+------------------------------+
| Content standard | Rule no. | AtoM field label | Information area             |
+==================+==========+==================+==============================+
| ISAD             | 3.5.3    | Related units of | Allied materials area        |
|                  |          | description      |                              |
+------------------+----------+------------------+------------------------------+
| DACS             | 6.3      | Related archival | Related materials elements   |
|                  |          | materials        |                              |
+------------------+----------+------------------+------------------------------+
| RAD              | 1.8B20   | Associated       | Notes area                   |
|                  |          | materials        |                              |
+------------------+----------+------------------+------------------------------+

However, as of AtoM 2.1, a new auto-complete :term:`field` has been added to
the :term:`edit page` of each of the above standards, that will allow users to
link an :term:`archival description` to another related description held in
AtoM. This linking is reciprocal - once it is added on one description, a link
back to the first resource will also appear on the related description.
Linking is managed via an auto-complete field: users begin to type the
identifier or title of a resource, and as they type, the auto-complete
:term:`drop-down <drop-down menu>` will display matching results.

In each standards template, the linking field appears just below the free-text
fields listed in the table above. It is labelled as "Related descriptions" in
the :ref:`ISAD <isad-template>` and :ref:`DACS <dacs-template>` templates, and
as "Related materials" in the :ref:`RAD <rad-template>` template.

.. figure:: images/related-description-field.*
   :align: center
   :figwidth: 80%
   :width: 100%
   :alt: An image of related description field in the ISAD template

   In this example, the "Related description" linking field is shown below the
   ISAD 3.5.3 Related units of description field in the ISAD template.

**To link an archival description to another description in AtoM:**

1. First, navigate to the :term:`archival description` where you wish to add a
   link. You can do this by :ref:`browsing <browse>` or
   :ref:`searching <search-atom>` for the :term:`archival description` - see
   :ref:`access-content` for more information on navigation in AtoM.

2. Switch from :term:`view mode` to :term:`edit mode` by clicking "Edit"
   button in the :term:`button block`, or by clicking on one of the
   :term:`information area` headings; this takes you to the record's
   :term:`edit page`.

.. image:: images/button-block-description.*
   :align: center
   :width: 75%
   :alt: An image of the button block on an archival description view page

3. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on an
   :term:`area header` to expand it and make changes. Use the table above to
   determine which information area will have the related descriptions field,
   based on which descriptive template (ISAD, RAD, DACS) you are using. For
   more information on working with content standards and descriptive
   templates in AtoM, see:

   * :ref:`descriptive-standards`
   * :ref:`change-display-standard`
   * :ref:`data-entry`
   * :ref:`default-templates`

.. image:: images/description-collapsed.*
   :align: center
   :width: 80%
   :alt: An archival description with all information areas closed

4. In the Related descriptions :term:`field`, begin typing either the
   identifier, full reference code, or title of the
   :term:`archival description` to which you would like to create a link. As
   you type, the field's :term:`drop-down menu` will provide auto-complete
   matching results. When you see the description to which you would like to
   create a link, click on it in the drop-down menu.

.. image:: images/add-related-description.*
   :align: center
   :width: 80%
   :alt: Using the related descriptions field to find another description

5. You can repeat this process to add multiple links to different descriptions
   at the same time.

.. image:: images/add-second-related-description.*
   :align: center
   :width: 80%
   :alt: Using the related descriptions field to find a second description

6. To **remove** a linked description, place your cursor over the bullet next
   to the linked description - it will change into an **X**. Click the **X**
   to remove the link to the related description.

.. image:: images/remove-related-description.*
   :align: center
   :width: 80%
   :alt: Removing a related description link

7. When you are finished adding or editing your related descriptions, click
   "Save" in the :term:`button block` at the bottom of the :term:`edit page`.
   Alternately, if you click "Cancel" or navigate away from the page without
   saving, none of your changes will be saved.

.. image:: images/button-block-save.*
   :align: center
   :width: 75%
   :alt: An image of the button block

8. Upon saving, AtoM will redirect you to the :term:`view page` for your
   :term:`archival description`. You will be able to see a link to the related
   description in the relevant :term:`information area` of your display
   template.

.. image:: images/related-description-view.*
   :align: center
   :width: 80%
   :alt: A related description link as seen in the view page

9. Similarly, AtoM will automatically add a reciprocal link back to the
   original description on the view and edit pages of the related resource.
   You can edit or remove the link by entering :term:`edit mode` on either
   description, and following instructions to remove a link in Step 6, above.

.. image:: images/related-description-reciprocal.*
   :align: center
   :width: 80%
   :alt: A related description link as seen in the view page

:ref:`Back to top <archival-descriptions>`

.. _change-display-standard:

Change the display standard
===========================

AtoM's :term:`archival description` edit templates are based on known standards
used within the cultural heritage community. For more information on
standards used in AtoM, see: :ref:`descriptive-standards`.

You can change the :term:`display standard` for an individual archival
description in the adminstration area while editing an archival description.
This allows you to choose a different description template per archival
description than the template you have chosen in your AtoM
:ref:`settings <default-templates>`. This includes at different levels of the
same :term:`archival unit` - so for example, if you have an image collection,
you could create a :term:`fonds`-level description using the
:ref:`ISAD <isad-template>` template, and then display all of the item-level
image descriptions using the :ref:`Dublin core <dc-template>` template.

You can also choose to have the newly selected display standard be inherited
by all :term:`child records <child record>` (for example, all the file-level
children beneath a series) if desired, or you can simply change the current
description. Instructions are included below.

**To change the display template of a description in AtoM:**

1. First, navigate to the :term:`archival description` you wish to edit. You
   can do this by :ref:`browsing <browse>` or :ref:`searching <search-atom>`
   for the :term:`archival description` - see :ref:`access-content` for more
   information on navigation in AtoM.
2. Switch from :term:`view mode` to :term:`edit mode` by clicking "Edit"
   button in the :term:`button block`, or by clicking on one of the
   :term:`information area` headings; this takes you to the record's
   :term:`edit page`.

.. image:: images/button-block-description.*
   :align: center
   :width: 85%
   :alt: An image of the button block on an archival description view page

3. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on the
   :term:`Administration area` heading to expand it and make changes.

.. image:: images/description-collapsed.*
   :align: center
   :width: 85%
   :alt: An archival description with all information areas closed

4. In the :term:`Administration area`, click the :term:`drop-down menu`
   labelled "Display standard". You will see a list of all display standards
   for archival descriptions available in AtoM. For more information on standards
   available in AtoM, see: :ref:`descriptive-standards`. For specific
   information on each standard, see: :ref:`data-entry`.

.. image:: images/change-display.*
   :align: center
   :width: 80%
   :alt: Option to change the display standard while editing an archival
         description

5. If you are currently using the default display template (see:
   :ref:`settings <default-templates>`), the field will be blank until you
   select a different template. Select the display standard you would like to
   use from the :term:`drop-down menu`.
6. If you would like all lower levels of description (e.g.
   :term:`child records <child record>`) to adopt the new display standard as
   well, click on the check-box below the template drop-down.
7. You can quit the create process at any time by clicking the "Cancel" button
   in the :term:`button block`; no new record will be created. Note that
   simply navigating away from the page by any other means, **without first
   clicking "Create"** will also result in no new record being created.
8. To save the record and display it with the new standards template, click
   the "Save" button located in the :term:`button block` at the bottom of
   the record.

.. image:: images/button-block-save.*
   :align: center
   :width: 85%
   :alt: An image of the button block

:ref:`Back to top <archival-descriptions>`

.. _add-alternative-id:

Add alternative identifiers to an archival description
======================================================

As of AtoM 2.1, users can now add alternative identifiers to descriptions
using the :ref:`ISAD(G) <isad-template>`, :ref:`RAD <rad-template>`, or
:ref:`DACS <dacs-template>` standards-based description templates. This can be
useful for keeping track of legacy identifiers or other relevant alphanumeric
strings associated with the identification of your records, such as a bar
code. To learn more about the description standards templates available in
AtoM, see the following:

* :ref:`descriptive-standards`
* :ref:`change-display-standard`
* :ref:`data-entry`
* :ref:`default-templates`

**To add an alternative identifer to your archival description:**

1. First, navigate to the :term:`archival description` you wish to edit. You
   can do this by :ref:`browsing <browse>` or :ref:`searching <search-atom>`
   for the :term:`archival description` - see :ref:`access-content` for more
   information on navigation in AtoM.
2. Switch from :term:`view mode` to :term:`edit mode` by clicking "Edit"
   button in the :term:`button block`, or by clicking on one of the
   :term:`information area` headings; this takes you to the record's
   :term:`edit page`.

.. image:: images/button-block-description.*
   :align: center
   :width: 75%
   :alt: An image of the button block on an archival description view page

3. On loading, the :term:`edit page` displays the record with all
   :term:`information areas <information area>` closed; click on the
   :term:`Administration area` heading to expand it and make changes.

.. image:: images/description-collapsed.*
   :align: center
   :width: 80%
   :alt: An archival description with all information areas closed

4. You will a link to reveal the Alternative identifiers field below the
   Identifier field, whose location depends on which display standard you are
   using (ISAD, RAD, or DACS). In general, it will be found in the first
   :term:`information area` of the description template.

+------------------+------------------------------+
| Content standard | Information area             |
+==================+==============================+
| ISAD             | Identity area                |
+------------------+------------------------------+
| RAD              | Title and statement of       |
|                  | responsibility area          |
+------------------+------------------------------+
| DACS             | Identity elements            |
+------------------+------------------------------+

.. figure:: images/alt-id-link.*
   :align: center
   :figwidth: 80%
   :width: 100%
   :alt: An image of the alternative identifier field in ISAD

   In this example, the link to reveal the Alternative identifier fields is
   found under the Identifier :term:`fields <field>` in the Identity
   :term:`information area` of the ISAD(G) template.

5. Click on the link to reveal the Alternative identifier fields below. Users
   can add a custom label (to describe the purpose or origin of the
   alternative identifier), and a value.

.. image:: images/alt-id-fields.*
   :align: center
   :width: 80%
   :alt: Fields revealed when the alternative identifier link is clicked

6. You can add multiple alternative identifiers at the same time, and you can
   return in :term:`edit mode` at any point in the future to edit, remove, or
   add new identifiers. To **add** another row, click the "Add new" link
   beneath the fields. To **remove** an alternative identifier, click the
   **X** to the right of the field row.

.. image:: images/alt-id-multiple.*
   :align: center
   :width: 80%
   :alt: Adding multiple alternative identifiers

7. When you are done adding, editing, or removing your alternative
   identifiers, click "Save" in the :term:`button block` located at the bottom
   of the :term:`edit page`. If you click "Cancel" or navigate away from the
   page without clicking "Save," you changes will not be saved.

.. image:: images/button-block-save.*
   :align: center
   :width: 75%
   :alt: An image of the button block

8. AtoM will redirect you to the :term:`view page` for your
   :term:`archival description`. The alternative identifiers will be displayed
   with their custom labels in the Notes :term:`area <information area>` of
   your descriptive template.

.. image:: images/alt-id-view-page.*
   :align: center
   :width: 80%
   :alt: Alternative IDs as displayed in the view page of a description

:ref:`Back to top <archival-descriptions>`

.. _move-archival-description:

Move an archival description
============================

Occasionally a user will need to move an archival description from one level
of description to another, from one :term:`fonds` or :term:`collection`
(or other top-level description) to another, or simply to change the
sort order within a number of records that share the same :term:`level of
description` (sometimes called siblings). There are two methods of moving
:term:`archival descriptions <archival description>` - the first method
allows only for changing the sort order in the :term:`treeview` found in the
:term:`context menu`, while the second method, more robust, allows for a
record to be moved broadly throughout the application, even allowing a lower
level of description to be moved so that it becomes a new :term:`parent
description <parent record>`.

.. _change-sort-order:

Method 1: Change sort order
---------------------------

This method **only** applies when there are multiple :term:`children
<child record>` with the same :term:`level of description` beneath a
:term:`parent description <parent record>` - i.e. "siblings". It will
change the sort order as displayed in the :term:`treeview` found in the
:term:`context menu` of the related descriptions. Users can drag-and-drop
children within the same level, for example moving series 02 above series 01
or moving items around within the same file. This is useful for users managing
the intellectual :term:`arrangement` of an :term:`archival unit`.

.. IMPORTANT::

   To be able to change the sort order, an :term:`administrator` **must**
   change the "Sort treeview" settings (located in **Admin > Settings >
   Global > Sort treeview**) to "Manual". Otherwise the drag and drop
   capabilities of the :term:`treeview` are disabled. For more information,
   see :ref:`Settings <settings>`.

**To change the sort order of sibling descriptions in the treeview:**

1. Navigate to the :term:`child description <child record>` whose sort order
   you wish to change. You can do this by :ref:`browsing <browse>` or
   :ref:`searching <search-atom>` for the :term:`archival description` - see
   :ref:`Access content <access-content>` for more information on navigation
   in AtoM.
2. In the :term:`treeview` located in the :term:`context menu` on the left-
   hand side of the record's :term:`view page`, the current record being
   displayed in the :term:`view page` will be highlighted by a dark grey bar.
   For more information on the treeview, see: :ref:`context-menu-treeview`.
3. In the :term:`treeview`, hover your cursor over the sibling record you wish
   to move - it can be any record on the same :term:`level of description` as
   the one currently being viewed.
4. If the "Sort treeview" setting has been set to "Manual" by an
   :term:`administrator` in **Admin > Settings > Global > Sort treeview**,
   then you will see three horizontal lines or bars appear on the right-hand
   side of the record-title you are hovering over in the treeview. This means
   the item can be dragged and dropped to a new sort order.
5. Click on the record in the treeview and hold, and then drag it to the new
   position you would like it to have in the treeview. Remember, you can move
   it to another position within the same :term:`level of description`, but
   the record will **not be moved** if you attempt to drag it from a lower to a
   higher level (e.g., from an item level to a file level, from a file level
   to a series or fonds level, etc.)
6. The record in the treeview will drop into its new location. No changes will
   occur on the :term:`view page` of the current record, though the sort order
   has been changed within the collection. You can repeat these steps as many
   times as are necessary to achieve the sort order you wish.

.. NOTE::

   Changing the sort order of a description with associated lower levels of
   description (i.e. :term:`children <child record>`) will also move the
   description's children. For example, if File 03, which has 10 item-level
   children, is dragged above File 01 to change the sort order, all of File
   03's children will also be moved, and will stay associated with File 03.


.. _move-different-level:

Method 2: Move a description to a different level
-------------------------------------------------

An authenticated (i.e. logged in) user with the proper permissions (see:
:ref:`User roles <user-roles>` and :ref:`edit-user-permissions`)
can also move a description from one level to another, or even from one
:term:`fonds` or :term:`collection` (or other top-level description), by
using the "Move" button located in the :term:`button block` of an
:term:`archival description's <archival description>` :term:`view page`. A
lower level of description can also be moved so that it becomes a new
:term:`parent <parent record>` description.

.. IMPORTANT::

   Moving any description using this method also moves all :term:`child-level
   descriptions <child record>` of the description being moved. For example,
   if you move a series that has file-level descriptions attached, all the
   file-level descriptions will be moved along with the series.

   If you wanted to move a description **without** moving all of its
   children, you could 1) Create a duplicate of the description 2) Move the
   duplicate record to its new position, and then 3) Edit the original
   description (with the children). See above,  :ref:`Duplicate an existing
   archival description <duplicate-archival-description>`.


**To move an archival description:**

1. Navigate to the :term:`child description <child record>` that you wish to
   move. You can do this by :ref:`browsing <browse>` or
   :ref:`searching <search-atom>` for the :term:`archival description` - see
   :ref:`Access content <access-content>` for more information on navigation
   in AtoM.
2. At the bottom of the description's :term:`view page`, press the "Move"
   button, located in the :term:`button block`.

.. image:: images/button-block-description.*
   :align: center
   :width: 85%
   :alt: An image of the button block on an archival description view page

3. You will be redirected to the Move page, which lists all top-level (i.e.
   :term:`parent <parent record>`) descriptions, and provides a search bar.
4. To find your move location more quickly ou can use the Move search bar to
   bring up results in the Move browse results listed below. For example, if
   you don't know the name of a series record but you do know the name of the
   :term:`fonds` or :term:`collection`, you could search for the top-level
   description and then use the Move browser (below) to navigate to the
   correct level of description.

.. image:: images/move-description.*
   :align: center
   :width: 85%
   :alt: An image of the move page

5. The blue hyperlinks allow Users to drill down into the hierarchy of the
   :term:`archival description` selected.  Clicking on a top-level description
   in the Move page will display the description's lower levels of description
   - for example, clicking on a :term:`fonds` would reveal the series or sous-
   fonds below it, and clicking on the series would then reveal the files
   below it. To orient yourself, a :term:`breadcrumb trail` will appear above
   the list of potential archival descriptions, indicating where in the
   :term:`archival unit's <archival unit>` you are currently located -
   this is intented to help Users understand if they are moving the record to
   a sous-fonds, series, sub-series, or a file.

.. image:: images/move-breadcrumb.*
   :align: center
   :width: 85%
   :alt: An image of the breadcrumb trail on a move page

6. If there are no more lower-level descriptions beneath the current level you
   are exploring in the move browser, then the move browser will be empty, as
   you can no longer drill down any lower in the hierarchy.

.. image:: images/move-no-lower.*
   :align: center
   :width: 85%
   :alt: An image of the move browser, showing a lowest level of description

7. When you have reached the right level where you want to move the record,
   the new :term:`parent description<parent record>` should be the last
   breadcrumb in the :term:`breadcrumb trail`, while the new siblings will be
   listed as hyperlinks below. Click "Move here" in the :term:`button block`
   to move the record.

.. image:: images/button-block-move.*
   :align: center
   :width: 75%
   :alt: An image of the button block on a move page

8. To make a child-level description a top-level description (e.g. to turn a
   series into a :term:`fonds`), click "Move here" **without** selecting one
   of the blue links.
9. You will be redirected to the moved record's :term:`view page`. If you look
   at the :term:`treeview` located in the :term:`context menu` on the left-
   hand side of the description's view page, you will see that your
   description has been moved to a new location.


:ref:`Back to top <archival-descriptions>`

.. _delete-archival-description:

Delete an archival description
==============================

An authenticated (i.e. logged in) user with the proper permissions (see:
:ref:`User roles <user-roles>` and :ref:`edit-user-permissions`)
can delete an :term:`archival description` at any time, by navigating to the
description and using the :term:`Delete button` located in the
:term:`button block`.

.. IMPORTANT::

   **Consequences of deleting an archival description in AtoM:**

   * If the record has lower-level descriptions registered to it, **all the
     lower-level records are also deleted** - i.e. if you delete a series, any
     sub-series, files, or items that belong to the series will also be
     deleted
   * Any date :term:`events <event>` (i.e. date(s) of creation, of
     publication, of contribution, etc.) associated with the description are
     deleted
   * The :term:`authority record` of the associated :term`creator` is **not**
     deleted
   * The :term:`archival institution` record of the associated
     :term:`repository` is **not** deleted

**To delete an archival description:**

1. Navigate to the :term:`archival description` that you would like to
   permanently delete. You can do this by :ref:`browsing <browse>` or
   :ref:`searching <search-atom>` for the :term:`archival description` - see
   :ref:`Access content  <access-content>` for more information on navigation
   in AtoM.
2. Scroll to the bottom of the description's :term:`view page`, and click the
   :term:`Delete button` located in the :term:`button block`.

.. image:: images/button-block-description.*
   :align: center
   :width: 85%
   :alt: An image of the button block on an archival description view page

3. AtoM will provide a warning and prompts you to confirm that you really wish
   to delete the description. If :term:`child descriptions <child record>`
   will be deleted as well,the warning will list them. If you are sure you
   want to delete the record and all of its descendants/children, click
   "Delete".

.. image:: images/description-delete-warning.*
   :align: center
   :width: 85%
   :alt: An image of a description delete warning

.. WARNING::

   Deleting a description is a permanent operation that cannot be undone, and
   the associated data will be removed from AtoM's database. Be sure that you
   want to delete a record before confirming the operation.

4. AtoM deletes the record and returns you to the :term:`parent record` of the
   deleted description or to the browse page if the deleted record was a top-
   level description.

:ref:`Back to top <archival-descriptions>`
