ZFS Configuration
=================

#. First set up ZFS by installing it:
   
    .. code-block:: bash

        example@example~ sudo apt-get repository ppa:zfs-native/stable

#. Now run the following command:
   
    .. code-block:: bash

        example@example~ sudo apt update

#. Finally install file system by command:
   
    .. code-block:: bash
        
        example@example~ sudo apt-get install -y ubuntu-zfs

#. The ZFS module are not loaded. Try running '/sbin/modprobe zfs' as a root to load them:
   
    .. code-block:: bash

        example@example~ sudo /sbin/modprobe zfs
    
#. Start by taking two of our hard disks and putting them in a storage pool by running the following command:

    .. code-block:: bash

        example@example~ sudo zpool create -f datapool /devs/sdb /dev /sdc

    .. note:: 
       zpool create is the command used to create a new storage pool, -f overrides any error that occur(such as if the disk(s) already have information on them), datapool is the name of the storage pool, and /dev/sdb /dev /sdc are the hard drive we put in the pool.

#. Run df -h check the zpool is created or not:
   
    .. code-block:: bash

        example@example~ df -h

#. Check status:
  
    .. code-block:: bash

        example@example~ sudo zpool status

#. Create a dataset:
   
    .. code-block:: bash

        example@example~ sudo zfs create datapool/datreon

#. Set mountpoint by using following command:

    .. code-block:: bash
    
        example@example~ Sudo zfs set mountpoint=/home/datreon datapool/datreon
    
#. Add user to the system by following command:
  
    .. code-block:: bash

        example@example~ sudo useradd -d /home/datreon -s /bin/bash/datreon datreon    
    

#. Change ownership the command:
 
    .. code-block:: bash

        example@example~ sudo chown -R datreon:datreon /home/datreon
    
#. Set desired password:
 
    .. code-block:: bash
      
        example@example~ sudo password
    
