# This is Python version 3.12.1

Copyright © 2001-2023 Python Software Foundation. All rights reserved.

See the end of this file for further copyright and license information.

Using Python
Installable Python kits, and information about using Python, are available at python.org.

Build Instructions
On Unix, Linux, BSD, macOS, and Cygwin:

./configure
make
make test
sudo make install
This will install Python as python3.

You can pass many options to the configure script; run ./configure --help to find out more. On macOS case-insensitive file systems and on Cygwin, the executable is called python.exe; elsewhere it's just python.

Building a complete Python installation requires the use of various additional third-party libraries, depending on your build platform and configure options. Not all standard library modules are buildable or useable on all platforms. Refer to the Install dependencies section of the Developer Guide for current detailed information on dependencies for various Linux distributions and macOS.

On macOS, there are additional configure and build options related to macOS framework and universal builds. Refer to Mac/README.rst.

On Windows, see PCbuild/readme.txt.

To build Windows installer, see Tools/msi/README.txt.

If you wish, you can create a subdirectory and invoke configure from there. For example:

mkdir debug
cd debug
../configure --with-pydebug
make
make test
(This will fail if you also built at the top-level directory. You should do a make clean at the top-level first.)

To get an optimized build of Python, configure --enable-optimizations before you run make. This sets the default make targets up to enable Profile Guided Optimization (PGO) and may be used to auto-enable Link Time Optimization (LTO) on some platforms. For more details, see the sections below.
