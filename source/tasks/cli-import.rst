.. _task-cli-data-import:

Import dummy data via cli
====================


Prerequisites
------------------

- :ref:`obp cli is installed<task-install-cli>`
- :ref:`obp cli is initalised<task-initialise-obp-cli>`
- Permissions

You may not have the correct permissions to perform the imports you want. The API will return an error specifying the permissions you need if you try to import data you don't have permissions for.


Concepts
-----------

To import data using the CLI you download the template spreadsheets 
provided, enter in as many rows as you want records, and then pass the
populated spredsheet to the cli.

-----------------------
Using Import Templates
-----------------------

The CLI provides spreadsheet templates which you populate with the data you wish you import. The purpose of this is to allow less technical users create a dataset which may easily be imported into the API. 

.. note:: 
  
  You must save your templates in the ".ods" file format.
  This is an open document standard, and the only format that the :code:`obp` cli currently
  supports. Once you've populated your template with your own data, be sure to save it as 
  :code:`.ods` format.

Locating import templates
''''''''''''''''''''''''''

The Open Bank Project provides import templates. Use these examples and edit them by adding rows of data for your
own desired dataset. 

The templates may currently be downloaded from the `OBP-CLI repo <https://github.com/OpenBankProject/OBP-CLI?files=1>`_.

Locate all the files ending in `.ods`. For example, at the time of writing, the users import template is called 
:code:`users-import-template-v1.ods` from the `repo <https://github.com/OpenBankProject/OBP-CLI/blob/cfb220777531ff033034d00922d9c54e69af781a/users-import-template-v1.ods>`_. 

.. warning::

  Be sure to check the latest master or release branch for the latest import templates.


Steps:

1. Take a template spreadsheet, for example "users.ods" and populate it with a list of users. 

2. Identify the correct CLI import command, for example for users import the command is: :code:`obp importusers users-import-template-v1.ods` press enter
3. If you have the correct permissions, and the data is valid, your import will succeed

If you don't have the correct permissions to create the object, then you may 
be able to use the cli to add roles for yourself, or request a higher 
privileged user grants them to you. See :code:`obp addrole --help`.
