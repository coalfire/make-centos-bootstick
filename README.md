# make-centos-bootstick

Generate a usb bootstick for CentOS.

Insert a usb stick (at least 1G) into a CentOS 7 machine.

Requirements:

 * rpm
 * syslinux
 * screen
 * dosfstools

```sh
yum -y install syslinux screen dosfstools
```

USAGE (as root): 

```sh
make-centos-bootstick [-r REMOTE_KS ] [-k LOCAL_KS] [-s CUSTOM_SYSLINUX] \
[-i ISO] [-u ISO_URL] [--no-clean] DEVICE
```

Any custom kickstart or syslinux.cfg need to be in your `$PWD`.

This probably works for and on any RedHat based distro,
but has only been tested with CentOS 7.

This is pretty much just https://gist.github.com/pauljeff/4b9ad551cb6c35870d7c
turned into a script.
