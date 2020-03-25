CDCBase Yocto - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_yocto.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions for Image (Hypervisor - Domain "SYS" on EVT1 - Hardware)**

    DISTRO=mentor-cdcbase . ./meta-mentor-cdcbase/setup-environment samsung-adk
    bitbake core-image-cdcbase

**Build Instructions for SDK (Hypervisor - Domain "SYS" on EVT1 - Hardware)**

    DISTRO=mentor-cdcbase . ./meta-mentor-cdcbase/setup-environment samsung-adk
    bitbake core-image-cdcbase:do_populate_sdk

**Build Instructions for Image + SDK (Hypervisor - Domain "SYS" on EVT1 - Hardware)**

    DISTRO=mentor-cdcbase . ./meta-mentor-cdcbase/setup-environment samsung-adk
    bitbake core-image-cdcbase core-image-cdcbase:do_populate_sdk
