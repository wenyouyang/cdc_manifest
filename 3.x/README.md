CDCBase Manifest for development of release-Branch 3.x
======================================================

This folder contains the manifests for the development of CDCBase release-Branch 3.x.


**Folders**

* android &rarr; This folder contains the (sub-) manifests for the android domain.
* autosar &rarr; This folder contains the (sub-) manifests for the autosar domain.
* yocto &rarr; This folder contains the (sub-) manifests for the yocto/linux domain.


**Manifests**

* cdcbase.xml &rarr; Main manifest used for development. This manifest includes the android/autosar/yocto - manifests.


**Sync Instructions**

    mkdir cdcbase
    cd cdcbase
    repo init -u ssh://stash.alm.mentorg.com:7999/cdcbase/cdcbase-manifests.git -b master -m 3.x/cdcbase.xml -g <Manifest-Group>,default
    GIT_SSH=ssh repo sync -j <Job-Count>

Please Note:

- To avoid issues with ssh-Implementation of our BitBucket-Server, it is recommended to set the environment variable 'GIT_SSH' to 'ssh' as a workaround.
- &lt;Job-Count> can be used to fetch the given number of repositories in parallel. It is recommended that it is set to a value <= 8. 
- &lt;Manifest-Group> can be used to fetch only a selected domain:
  - all
  - android
  - autosar
  - yocto

***Smart Mirror usage***

@TODO


**Build Instructions**

Please see the README.md file contained in the folders.
