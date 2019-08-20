.. _task-install-cli:

##############################
Install obp cli
##############################


.. note:: 
  The cli requires you use python version 3
  or higher. On some systems this means your
  pip is called `pip3` rather than `pip`

.. code-block:: sh

  pip3 install --user obp-python # Requires at least python 3


.. _verify-cli-install:

Verify installation
====================

.. code-block:: sh

  obp --help

Expected output:
'''''''''''''''''

.. code-block:: sh

  Usage: obp [OPTIONS] COMMAND [ARGS]...

  Options:
    --help  Show this message and exit.

  Commands:
    addaccount              📁 Add a bank account
    addbank                 🏦 Add a bank
    addcustomer             🧙 Add a customer
    addfx                   📉 Add exchange rate (FX)
    addrole                 🚧 Add a role for current user
    adduser                 📝 Add a user
    addview                 🧐 Add a view
    answerconsent           🚧 Answer consent
    createconsent           🚧 Add a consent
    deletebranches          ⚠️ 🏦 Delete all branches
    deletecardbyid          ⚠️ 💳 Delete card by id
    getaccountbyid          📁 Get account by id (includes balance)
    getaccountsheld         📁 Get list of accounts held
    getaccounttransactions  📁 Get transactions for an account
    getauth                 🔑 Get your DirectLogin token
    getbanks                🏦 Get list of banks
    getcardbyid             💳 Get card by id
    getcardbynumber         💳 Get card by card number
    getcards                💳 Get list of cards at bank
    getconsents             🚧 Get consents
    getconsentstatus        🚧 Get consent status- with certificate
    getcustomers            👥 Get list of customers
    getuser                 😃 Get your user info
    getuserid               📋 Get your user id
    getuseridbyusername     📋 Get user id by username
    getviews                🧐 Get views by provider
    importaccounts          🚜 Import accounts from spreadsheet template
    importbranches          🚜 Import branches from spreadsheet template
    importcardattribues     🚜 Import card attributes from spreadsheet template
    importcards             🚜 Import cards from spreadsheet template
    importcustomers         🚜 Import customers from spreadsheet template
    importtransactions      🚜 Import transactions from spreadsheet template
    importusers             🚜 Import users from spreadsheet template
    init                    💡 Initalize connection to your Open Bank Project...
    linkusertocustomer      🔗 Link user to a customer
    revokeconsent           🚧 Revoke consent
    sandboximport           🚜 Bulk import sandbox data from json input


Congratulations! If you see the help menu output, you have installed the obp    cli.

.. note:: 

  You can also view additional help on individual commands,
  such as :code:`obp addrole --help` to get more help on the
  :code:`addrole` command. For example:

    .. code-block:: sh

      obp addrole --help
      Usage: obp addrole [OPTIONS]

      🚧 Add a role for current user

      Options:
        --role-name TEXT  Name of the role/entitelment  [required]
        --bank-id TEXT    Some roles need a bank id
        --user-id TEXT    Add role to a differnt user
        --help            Show this message and exit.

