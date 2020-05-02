An Introduction To The ZFS File System(zfs) For Lunix
=====================================================

The z file system is a free & open source logical volume manager built by SUN Microsystems for use in their Solaris operating system. Some of its most appealing features includes:

Endless salability
------------------ 
It is a 128-bt file system that's capable of managing zettabytes(one billion terabytes) of data. ano matters how much hard drive space you have, zfs will be suitable for managing it.

Maximun integrity
-----------------
Everything one doees inside of ZFS uses a cheksun to ensure file integrity. One can rest assured that your file and their redudant copies will not encounter silent data corruption. Also, while ZFS is busy quitly checking your data for integrity, it will do automatic repairs anytime it can.

Drive pooling
-------------
The creator of ZFS want you to think of it as being similar to the way your computer uses RAM. When you need more memory in your computer, you put un another stick and you're done. No need to spend time partitioning, formatting initializing, or doing anything else to your disks- when you need a bigegr storage "pool," just add disks.

RAID
----
ZFS is capable of many different RAID levels, all while delivering performance that's comparable to that of hardware RAID controller. This allows you to save money, makes setup easier, and have access to superiop RIAD levels that ZFS has improves upon.

.. image:: zfsintro.png

.. code-block::  bash 

    datreon@~ sudo apt update

