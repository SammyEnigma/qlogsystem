This is qlogsystem, welcome.
============================

qlogsystem is a very efficient and easy to use logger library written in C++
(using the Qt framework). qlogsystem brings Java style logger hierarchy to C++
with a very simple API, which makes possible to use it in libraries too. With
a proper logger hierarchy log message can be categorized and filtered in
run-time. The format of the log messages and the output can be configured and
changed separately. qlogsystem is very fast. The log messages and their
parameters are evaluated only if the log level is big enough, so debug
messages will not affect the performance much. qlogsystem is thread safe, but
locking is done only when needed.

Key features:
  - easy to use, simple API
  - convenient log macros (messages with parameters)
  - very fast (late parameter evaluation)
  - threadsafe
  - java style logger hierarchy
  - unique id for log messages
  - log format and log output can be tweaked


Building instructions
=====================

Build dependencies:
  - Qt framework

Optional dependencies for coverage results and documentation:
 - lcov, gcov
 - doxygen, graphviz

Steps:

```
mkdir build && cd build
qmake ../project.pro CONFIG+=release PREFIX=$PWD/install
make
make install
```

See the documentation for further examples (e.g: how to run the tests.).
(`make docs`)


Installation Instruction (with qpm)
===================================

[qpm.io](https://qpm.io)

 1) Run `qpm install`

```
$ qpm install com.balabit.qlogsystem
```

 2) Include vendor/vendor.pri in your .pro file

```
include(vendor/vendor.pri)
```

 3) Add include statement in your C++ source files

```
#include <qlogsystem/qlogsystem.hh>
```


Documentation
=============

See doc/src/main.dox for details.


Licensing
=========

The project is licensed under the LGPL v2.1 license.

Copyright (c) BalaBit IT Ltd, Budapest, Hungary
