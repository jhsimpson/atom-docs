.. _rights:

======
Rights
======

As discussed in the section on entity types,
:term:`Rights records <rights record>` provide rights related restrictions
that can be linked to :term:`accession records <accession record>`,
:term:`archival descriptions <archival description>` and
:term:`digital objects <digital object>`. AtoM Rights metadata elements use
`PREMIS rights elements <http://www.loc.gov/standards/premis/>`__. In AtoM
restrictions can be based on Copyright(s), License, Statute(s) and Policy.
You can also include rights restrictions based on guidelines set by the
Donor of the records. Rights are inherited in AtoM, which means that rights
added at a higher level (e.g., fonds level) are inherited by the lower levels
(e.g., item level). If you add rights to an
:term:`accession record`, all
:term:`archival descriptions <archival description>` created from that
accession will inherit the same rights. If you add rights to an
:term:`archival description` at the :term:`fonds` or
:term:`collections <collection>` level, all lower levels (aka
:term:`child records <child record>`) such as the file or item-level will
inherit those rights.

Add a new rights record
=======================

This section describes how to add a new :term:`rights record` by using the
rights dialog provided through the add/edit template.

.. NOTE::
   You must be logged in and have the appropriate privileges, such as
   :term:`editors` and :term:`administrators` to be able to add/edit content
   in AtoM, which includes creating a :term:`rights record`.
   See: :ref:`Log in <log-in>`.

Add rights to a new Accession record
------------------------------------

.. figure:: images/accession-rights.png
   :align: right
   :figwidth: 50%
   :width: 100%
   :alt: Rights record dialogue box in edit accession record page

   Rights record dialogue box in edit accession record page.


1. Navigate to the :term:`main menu` located in the :term:`header bar`, click
   the "Add" menu and select :term:`accession record` from the
   :term:`drop-down menu`.

2. AtoM takes you to a blank :term:`edit page` for data entry for an
   :term:`accession record`.

3. On loading, the :term:`edit page` displays the accession record with the
   first :term:`information area` open, Basic info. You can begin entering
   information about your new accession.

4. To enter Rights information, scroll down the page until you see the
   :term:`information area` titled, Rights area, click on it to access the
   :term:`rights record` dialogue.

5. Click on the "Add new" button and the default :term:`rights record`
   dialogue box will pop up.

6. The "Act" data entry field is a drop-down list. You can select: Delete,
   Discover, Display, Disseminate, Migrate, Modify, and Replicate.

7. The "Restriction" data entry field provides two choices: Allow or
   Disallow.

8. You can add a Rights holder name, or select an existing one using the
   auto-complete action provided by AtoM.

9. You can add a Rights note, describing any additional information about the
   Rights holder that might not already exist in their Rights holder record.

10. The "Basis" data entry field is a drop-down list. You can select:
    Copyright, License, Statute, Policy, or Donor. Depending upon your
    selection, the AtoM Right record dialogue provides additonal data entry
    fields.

11. Once you complete adding information to the rights record, click on the
    blue Submit button and then click on the blue Create button to save the
    new accession record. If you have already created the accession record,
    and you are editing the rights information, you will click on the blue
    Save button.

Add rights to a new Archival description
----------------------------------------

.. figure:: images/archdescription-rights.*
   :align: right
   :figwidth: 50%
   :width: 100%
   :alt: Rights record dialogue box in edit archival description page

   Rights record dialogue box in edit archival description page.


1. Navigate to the :term:`main menu` located in the :term:`header bar`,
   click the "Add" menu and select :term:`archival description` from the
   :term:`drop-down menu`.

2. AtoM takes you to a blank :term:`edit page` for data entry for an
   :term:`archival description`.

3. On loading, the :term:`edit page` displays the archival description with
   all the :term:`information areas <information area>`, closed. The name of
   the first :term:`information area` will vary according to the archival
   content standard you are using. In the example shows, ISAD(G) is shown.
   You can begin entering information about your archival description.

4. To enter Rights information, scroll down the page until you see the
   :term:`information area` titled, Rights area, click on it to access the
   :term:`rights record` dialogue.

5. Click on the "Add new" button and the default :term:`rights record`
   dialogue box will pop up.

6. The "Act" data entry field is a drop-down list. You can select: Delete,
   Discover, Display, Disseminate, Migrate, Modify, and Replicate.

7. The "Restriction" data entry field provides two choices: Allow or
   Disallow.

8. You can add a Rights holder name, or select an existing one using the
   auto-complete action provided by AtoM.

9. You can add a Rights note, describing any additional information about the
   Rights holder that might not already exist in their Rights holder record.

10. The "Basis" data entry field is a drop-down list. You can select:
    Copyright, License, Statute, Policy, or Donor. Depending upon your
    selection, the AtoM Right record dialogue provides additonal data entry
    fields.

11. Once you complete adding information to the rights record, click on the
    blue Submit button and then click on the blue Create button to save the
    new archival description. If you have already created the archival
    description, and you are editing the rights information, you will click
    on the blue Save button.


  .. figure:: images/recordrights.*
   :align: right
   :figwidth: 50%
   :width: 100%
   :alt: View rights added to archival description

   View rights added to archival description.


12. In the example provided on the right, you are viewing the completed
    archival description and can see that a rights record (copyright) has
    been added.

:ref:`Back to top <rights>`