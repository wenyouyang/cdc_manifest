CDCBase Android - Manifest of release 2.0
=========================================

This folder contains the manifest for android of CDCBase release 2.0.


**Manifest**

* cdcbase_android.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions**

     unset CROSS_COMPILE
    ./build.sh <Target> eng

With <Target>:

- sadkHR80_evt1 &rarr; Android Baremetal evt1
- rbvmsiSadkHR80_evt1 &rarr; IVI VM evt1 (android)
