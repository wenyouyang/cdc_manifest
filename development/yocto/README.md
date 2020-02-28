CDCBase Yocto - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_yocto.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions for Baremetal**

    export TEMPLATECONF=$PWD/meta-mentor-samsung-bsp/conf/bare_<variant>/
    . ./poky/oe-init-build-env
    bitbake core-image-bare

With &lt;variant>:

* "evt0"
* "evt1"


**Build Instructions for Hypervisor - Domain "SYS"**

    export TEMPLATECONF=$PWD/meta-mentor-samsung-bsp/conf/sys_<variant>/
    . ./poky/oe-init-build-env
    bitbake sys-domain

With &lt;variant>:

* "evt0"
* "evt1"
