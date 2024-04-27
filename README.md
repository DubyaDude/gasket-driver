# Coral Gasket Driver Build
This repository is meant to distribute an updated build of the Coral Gasket Driver as the package has not been updated for some time, making it difficult to install on newer versions.

## How to install
- Purge any previous versions of `gasket-dkms` you may have installed.
- Go to releases and download the latest release.
  - Inside the zip, you will need the `gasket-dkms_X_all.deb` where `X` is the version number.

- Run either of the following to install the package:
  - `dpkg -i ./gasket-dkms_X_all.deb`
  - `apt install ./gasket-dkms_X_all.deb`


# Coral Gasket Driver

The Coral Gasket Driver allows usage of the [Coral EdgeTPU](https://coral.ai/) on Linux systems. The driver contains two modules:

* Gasket: Gasket (Google ASIC Software, Kernel Extensions, and Tools) is a top level driver for lightweight communication with Google ASICs.
* Apex: Apex refers to the [EdgeTPU v1](https://coral.ai/technology)

This repo contains both the source for direct integration into a kernel tree as well as the necessary files to generate a Debian DKMS package.

## Building Debian DKMS pacakge

From the top level directory, execute:

```
debuild -us -uc -tc -b
```
