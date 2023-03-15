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

**For Dockerfile**

    RUN apk --update add --no-cache\
        file \
        g++ \
        git \
        make \
        autoconf \
        boost-dev #or libboost-all-dev


    RUN docker-php-source extract \
        && git clone https://github.com/ArtUkrainskiy/php_boost_ipc /usr/src/php/ext/php_boost_ipc \
        && cd /usr/src/php/ext/php_boost_ipc && git submodule update --init \
        && docker-php-ext-install php_boost_ipc