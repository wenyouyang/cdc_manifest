CDCBase Android - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_android.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.


**Build Instructions**

     export WORKING_DIR=$pwd/android

     sudo apt-get install maven
     sudo apt-get install openjdk-8-jdk openjdk-8-jre

     cd $WORKING_DIR/external/capicxx-core-tools/org.genivi.commonapi.core.releng
     mvn -Dtarget.id=org.genivi.commonapi.core.target clean verify

     cd $WORKING_DIR/capicxx-someip-tools/org.genivi.commonapi.someip.releng
     mvn -Dtarget.id=org.genivi.commonapi.someip.target clean verify -DCOREPATH=$WORKING_DIR/external/capicxx-core-tools

     cd $WORKING_DIR
     . build/envsetup.sh
     lunch aosp_car_x86_64-userdebug
     make -j<NUMBER_OF_JOBS>
