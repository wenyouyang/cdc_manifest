CDCBase Yocto - Manifest for development
========================================

This folder contains the manifest for the yocto development of CDCBase.


**Manifest**

* cdcbase_yocto.xml &rarr; Main manifest used for yocto development.


**Sync Instructions**

Please see the README.md in the parent folder.

How to build a Image for a specific Machine
-------------------------------------------
    DISTRO=<distro> . ./meta-mentor-cdcbase/setup-environment [-l Optional Layers] [-b build-dir] <Machine>
    bitbake <image>

### Supported Machines
| Machine     | Layer                   | Target / Board                           | Hypervisor-Partition |
|:------------|:------------------------|:-----------------------------------------|:---------------------|
| samsung-adk | meta-mentor-samsung-bsp | Samsung Automotive Developmet Kit (evt1) | System (sys)         |

### Supported Distros
| Disto          | Layer               |
|:---------------|:--------------------|
| mentor-cdcbase | meta-mentor-cdcbase |

### Supported Images
| Image              | Layer               |
|:-------------------|:--------------------|
| core-image-cdcbase | meta-mentor-cdcbase |

### Optional Layers
| Layer                  | Description                                 |
|:-----------------------|:--------------------------------------------|
| mentor-cdcbase-testing | Recipes to build tests and the test-tarball |


How to build a SDK for a specific Machine
-----------------------------------------
The SDK can be build through the task 'do_populate_sdk' of the image recipe:

    bitbake <image>:do_populate_sdk

This can also combined into a single call, to build the image and the SDK in one run:

    bitbake <image> <image>:do_populate_sdk
