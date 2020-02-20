CDCBase Yocto - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_yocto.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions**   

    export TEMPLATECONF=$PWD/meta-mentor-samsung-bsp/conf/evt0/
    . ./poky/oe-init-build-env
    bitbake core-image-bare
