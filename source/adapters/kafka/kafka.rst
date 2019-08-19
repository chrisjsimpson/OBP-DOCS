================
Kafka Adapter
================

The Kafka connector provides the following advantages when connecting OBP to a core banking system.

- It provides a logging layer for non repudiation. i.e. OBP sent this request to the core banking system at this time. The messages can be consumed into another (offsite) storge system.

- It provides a layer for real time analytics / fraud monitoring. i.e. Apache Spark or other tools could monitor the queue and look for irregularities.

- It provides a separation from the core OBP API. i.e. it's easier to use the OBP API develop branch when using the Kafka connector.

- Connector Code (south of the Kafka queue) is not restricted to a JVM language (Scala, Java, Clojure etc.) You can use any language that speaks Kafka e.g. Python, Go, C# etc.

.. code-block:: sh:

       OBP
        |
    North side connector (Scala or any JVM language)
      Kafka
    South side connector (Any language)
        | 
    Core Banking

