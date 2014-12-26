libdatastruct
=============

*libdatastruct* is a portable library providing the **container data structures** of the [GNU Portability Library][GNU Gnulib] (*Gnulib*).

The following data structures are provided.

Data Structure | Description
--- | ---
*list* | Abstract sequential list data type
*xlist* | Abstract sequential list data type, with out-of-memory checking
*array-list* | Sequential list data type implemented by an array
*carray-list* | Sequential list data type implemented by a circular array
*linked-list* | Sequential list data type implemented by a linked list
*avltree-list* | Sequential list data type implemented by a binary tree
*rbtree-list* | Sequential list data type implemented by a binary tree
*linkedhash-list* | Sequential list data type implemented by a hash table with a linked list
*avltreehash-list* | Sequential list data type implemented by a hash table with a binary tree
*rbtreehash-list* | Sequential list data type implemented by a hash table with a binary tree
*sublist* | Sequential list data type backed by another list
*xsublist* | Sequential list data type backed by another list, with out-of-memory checking
*oset* | Abstract ordered set data type
*xoset* | Abstract ordered set data type, with out-of-memory checking
*array-oset* | Ordered set data type implemented by an array
*avltree-oset* | Ordered set data type implemented by a binary tree
*rbtree-oset* | Ordered set data type implemented by a binary tree

The source code directly utilitises the [source][GNU Gnulib source] of Gnulib.

Building
--------

To build the library, simply run `./build` from the root directory of the project. This produces all output in the `output` subdirectory.

Installing
----------

To install the library, first build it, then run `./install` as superuser from the root directory of the project. This will install the library under the default prefix directory `/usr/local`.

A custom prefix directory can be specified by setting the `INSTALL_PREFIX` environment variable before installing.

Usage
-----

The API is not explicitly documented, but can be determined via the header files in the `include` directory within the project. In addition, the source code itself is commented; it may be found in the `gnulib/gllib` directory.

Updating Source Code
--------------------

An imported version of the source code for the Gnulib modules is contained within the project directory. If you wish to update this imported version to the latest source for Gnulib, you first need to obtain a copy of [Gnulib][GNU Gnulib]. This package contains the source for GNU code (including the relevant modules), along with the program [`gnulib-tool`][GNU gnulib-tool], which can import such GNU code into a separate project.

To update the imported source code, first ensure that the `gnulib-tool` program of *Gnulib* (or a symbolic link pointing to it) can be found via `PATH` environment variable. Then simply run `./update-source` from the root directory of the project. You will be notified whether the update succeeds or fails; if it fails then the previous imported source will remain intact.

[GNU Gnulib]: https://www.gnu.org/software/gnulib/
[GNU Gnulib source]: http://git.savannah.gnu.org/gitweb/?p=gnulib.git
[GNU gnulib-tool]: https://www.gnu.org/software/gnulib/manual/html_node/Invoking-gnulib_002dtool.html
