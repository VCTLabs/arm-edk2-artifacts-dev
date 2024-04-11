EDK II socfpga Artifacts
========================

Basic workflow for cloning and building the Intel(altera) UEFI
repos for Arria10 dev boards.

From Intel EDK-2 links:

* https://www.intel.com/content/www/us/en/docs/programmable/683735/current/arria-10-soc-boot-user-guide.html
* https://github.com/altera-opensource/uefi-socfpga
* https://github.com/altera-opensource/edk2-platforms-socfpga

RocketBoards

* https://www.rocketboards.org/foswiki/Main/WebHome

Building EDK2

* https://stackoverflow.com/questions/63725239/build-edk2-in-linux

Both tianocore and altera upstream repos use ubuntu-latest as one of their
CI runners and install native/cross platform compilers. There is also a long
list of package deps:

sudo apt install gcc g++ make uuid-dev nasm nuget iasl \
gcc-multilib-arm-linux-gnueabihf g++-multilib-arm-linux-gnueabihf \
nodejs curl lcov libx11-dev libxext-dev python3-distutils-extra \
python3-pip python3-setuptools npm

And the snap with dotnet-runtime-60:

$ sudo snap install dotnet-runtime-60

$ export GCC5_AARCH64_PREFIX="aarch64-linux-gnu-"
$ export GCC5_ARM_PREFIX="arm-linux-gnueabihf-"

