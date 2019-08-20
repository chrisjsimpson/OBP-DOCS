.. _task-initialise-obp-cli:

******************
Initalise obp cli
******************

To use the obp cli against an Open Bank Project instance, you must
first initalise it against the url of the instance you wish to access. 

Prerequisites:
****************

You must already have:

- :ref:`task-install-cli`


How to initialise your connection
**********************************

Type :code:`obp init`, you will then be asked to enter your 
Open Bank Project URL, username, password and consumer key 
(see :ref:`task_get-consumer-key`).

.. code-block:: sh

  obp init
  Please enter your API_HOST:  [https://api.example.com]: https://api.example.com
  Please enter your username:  [chris]: chris
  Please enter your password: 
  Repeat for confirmation: 
  ... generating direct login token
  Please enter your OBP_CONSUMER_KEY: abc123
  Init complete

Once you see :code:`Init complete`, your obp cli has been successfully initalised!
Verify your connection by running a simple command:

.. code-block:: sh

  obp getuser
  {"user_id":"uuid-hash","email":"chris@example.com","provider_id":"chris","provider":"https://apisandbox.openbankproject.com","username":"chris","entitlements":{"list":[]},"views":{"list":[]}}

The response should be your user object. See :ref:`verify-cli-install` for a
selection of possible commands.



