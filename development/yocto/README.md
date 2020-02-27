CDCBase Yocto - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_yocto.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions**   

    export TEMPLATECONF=$PWD/meta-mentor-samsung-bsp/conf/<variant>/
    . ./poky/oe-init-build-env
    bitbake core-image-bare

With &lt;variant>:

* "bare_evt0"	-	Baremetal for EVT0-Revision
* "bare_evt1"	-	Baremetal for EVT1-Revision
* "sys_evt0"	-	System Hypervisior-Partition for EVT0-Revision
* "sys_evt1"	-	System Hypervisior-Partition for EVT1-Revision
