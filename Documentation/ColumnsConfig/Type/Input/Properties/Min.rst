.. include:: /Includes.rst.txt
.. _columns-input-properties-min:

===
min
===

.. versionadded:: 12.0

.. confval:: min

   :Path: $GLOBALS['TCA'][$table]['columns'][$field]['config']
   :type: integer
   :Scope: Display

   This option allows to define a minimum number of characters for the
   :html:`<input>` field and adds a :html:`minlength` attribute to the field.
   If at least one character is typed in and the number of characters is less
   than :php:`min`, the FormEngine marks the field as invalid, preventing the
   user to save the element. DataHandler will also take care for server-side
   validation and reset the value to an empty string, if :php:`min` is not
   reached.

   When using :php:`min` in combination with :ref:`columns-input-properties-max`,
   one has to make sure, the :php:`min` value is less than or equal :php:`max`.
   Otherwise the option is ignored.

   Empty fields are not validated. If one needs to have non-empty values, it is
   recommended to use :php:`required => true` in combination with :php:`min`.
