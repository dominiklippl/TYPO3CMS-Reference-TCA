.. include:: /Includes.rst.txt
.. _ctrl-reference-label:

=====
label
=====

.. confval:: label (ctrl)

   :Path: $GLOBALS['TCA'][$table]['ctrl']
   :type: string (field name)
   :Scope: Display


   **Required!**

   Points to the field name of the table which should be used as the "title"
   when the record is displayed in the system.

   .. note::
      :ref:`label_userFunc <ctrl-reference-label-userfunc>` overrides this
      property (but it is still required).

   .. warning::
      For the label only regular input or text fields should be used. Otherwise
      issues may occur and prevent from a working system if
      :typoscript:`TCEMAIN.table.tt_content.disablePrependAtCopy` is not set or
      set to :typoscript:`0`.

A simple example
----------------

.. include:: /Images/Rst/TxStyleguideCtrlMinimal.rst.txt

.. include:: /CodeSnippets/TxStyleguideCtrlMinimal.rst.txt
