# binutils-cil  ![binutils-cil CI](https://github.com/BrickBot/binutils-cil/workflows/binutils-cil%20CI/badge.svg)
Used in conjunction with the gcc-cil project to add CIL capabilties, for use with
[brickOS-bibo](https://github.com/BrickBot/brickOS-bibo) and [Lego.NET](https://github.com/BrickBot/gcc-cil)


## Background
The starting point for the code in this repository is the version of
binutils 2.15 that was used in the creation of the Lego.NET v1.4 release.


For additional details, please refer to the README in the [gcc-cil project](https://github.com/BrickBot/gcc-cil).

## Note to Package Builders and Maintainers
To avoid conflicts with tool-prefix names for the “standard” cross-compile toolchain,
it is suggested to add “-cil” to the end of the prefix.

As an example, on Debian/Ubuntu, the standard prefix for h8/300 tools is `h8300-hms-`;
for these CIL-enabled build tools, it is suggested to make the prefix `h8300-hms-cil-`.


## 

The remainder of this file is the contents of the original binutils README file

* * *

# README for GNU development tools

This directory contains various GNU compilers, assemblers, linkers, 
debuggers, etc., plus their support routines, definitions, and documentation.

If you are receiving this as part of a GDB release, see the file gdb/README.
If with a binutils release, see binutils/README;  if with a libg++ release,
see libg++/README, etc.  That'll give you info about this
package -- supported targets, how to use it, how to report bugs, etc.

It is now possible to automatically configure and build a variety of
tools with one command.  To build all of the tools contained herein,
run the ``configure'' script here, e.g.:

	./configure 
	make

To install them (by default in /usr/local/bin, /usr/local/lib, etc),
then do:
	make install

(If the configure script can't determine your type of computer, give it
the name as an argument, for instance ``./configure sun4''.  You can
use the script ``config.sub'' to test whether a name is recognized; if
it is, config.sub translates it to a triplet specifying CPU, vendor,
and OS.)

If you have more than one compiler on your system, it is often best to
explicitly set CC in the environment before running configure, and to
also set CC when running make.  For example (assuming sh/bash/ksh):

	CC=gcc ./configure
	make

A similar example using csh:

	setenv CC gcc
	./configure
	make

Much of the code and documentation enclosed is copyright by
the Free Software Foundation, Inc.  See the file COPYING or
COPYING.LIB in the various directories, for a description of the
GNU General Public License terms under which you can copy the files.

REPORTING BUGS: Again, see gdb/README, binutils/README, etc., for info
on where and how to report problems.
