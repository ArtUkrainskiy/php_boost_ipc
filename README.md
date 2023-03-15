php_boost_ipc
====
**php_boost_ipc** - PHP extension for C++ Boost IPC.

It supports the following activities:
- Provides an interface for using the boost::unordered_map container located in shared memory.

Requirements
============

* PHP 7+

Installation
============

**From sources**

    phpize
    ./configure 
    make
    make install
Add ```extension=php_boost_ipc.so``` to your php.ini
