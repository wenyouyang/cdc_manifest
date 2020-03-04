CDCBase Yocto - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_yocto.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions (Hypervisor - Domain "SYS" on EVT1 - Hardware)**

    export TEMPLATECONF=$PWD/meta-mentor-samsung-bsp/conf/sys_evt1/
    . ./poky/oe-init-build-env
    bitbake sys-domain
