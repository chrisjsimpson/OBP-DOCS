.. _adapter-akka-intro:

===============
Akka Adapter
===============

Use Akka as an interface between OBP and your Core Banking System (CBS)
-------------------------------------------------------------------------

For an introduction to Akka see `Akka Docs <https://akka.io/>`_.

The OBP Akka interface allows integrators to write Java or Scala Adapters (any JVM language with Akka support)
respond to requests for data and services from OBP.

For the message definitions see [here](/message-docs?connector=akka_vDec2018)

----------------------------
Installation Prerequisites
----------------------------


* You have OBP-API running.

* Ideally you have API Explorer running (the application serving this page) but its not necessary - you could use any other REST client.
* You might want to also run API Manager as it makes it easier to grant yourself roles, but its not necessary - you could use the API Explorer / any REST client instead.

.. toctree::
  :maxdepth: 2       

  messages/messages.rst
  messages/akka-message-getAdapterInfo.rst
