# assignment_EL

rpi4 used for assignment

-clone the repository in the poky folder

-add meta-heartbeat to layers of the project with the following command

bitbake-layers add-layer meta-heartbeat

-add to local.conf the following lines

IMAGE_INSTALL_append = " heartbeat"
IMAGE_INSTALL_append = " kheartbeat"
KERNEL_MODULE_AUTOLOAD += "kheartbeat"

-start the bitbake core-image-full-cmdline

-setup the SD card

-on rpi create the associated device file with command like for example

mknod /dev/kheartbeat c 241 0

with the proper major number

-in the /usr/bin folder we can run the heartbeat executable
