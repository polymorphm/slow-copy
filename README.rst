README
======

``slow-copy`` is a micro utility to make copying files in *synchronous manner*.
You may be needed this utility when a copy target is a slow usb drive. The
utility supports coping of next file system objects:

    * Regular files
    * File directories (recursively)
    * Symbolic links
    * Modification time file attributes
    * File permissions attributes (basic)

Unlike the ``cp`` utility (from the ``coreutils`` package) the ``slow-copy``
utility can not rename a target file to another name different from from its
source file. And can not do a lot of other ``cp`` things.

``slow-copy`` just does file copying from one place to another place, and does
it **slowly** ;-) !

Status
------

The developer version (the git master branch).

Usage Example
-------------

If we want to copy a directory ``"Extra_English"`` to a USB flash drive
``"CA19-348B"``, we will do it like this:

::

    ./slow-copy -v -- '/home/regular-user/Videos/films/Extra_English' '/run/media/regular-user/CA19-348B'

The utility will create the directory
``/run/media/regular-user/CA19-348B/Extra_English`` with all its files.
