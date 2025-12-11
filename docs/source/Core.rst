Core
=====

this page details what you need to know about the core module. this modules is used as an api gateway, and takes into account 3 type's of communication
- Http/Rest
- GRPc
- Kafka consummers and producers

Pre-requisites
--------------
the technologies required to run this module are:

- vcpkg
- cmake


How to build
------------

.. code-block:: bash
   cmake -B build -S . -DCMAKE_TOOLCHAIN_FILE=/path/to/vcpkg/scripts/buildsystems/vcpkg.cmake

   cmake --build build

   # Release Build
   cmake --build build --config Release

Dependencies used in this module
--------------------------------

- librdkafka
- curl
- libwebsckets
- protobuf
- grpc
- libmicrohttpd

