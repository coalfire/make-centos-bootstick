# UNMAINTAINED.

See https://github.com/coalfire/cent-mkiso for a simpler (but less featureful) implementation.

# make-centos-bootstick

Generate a usb bootstick for CentOS,
optionally with a
custom kickstart or remote kickstart,
custom sysconfig (boot menu),
and custom splash image.

The default iso is CentOS 7.
The iso or mirror may be customized with command line flags.

## Requirements

 * rpm
 * syslinux
 * dosfstools

```sh
yum -y install syslinux dosfstools
```

## Usage (as root)

Insert a usb stick (at least 1G) into a CentOS 7 machine.

```sh
make-centos-bootstick [-r REMOTE_KS ] [-k LOCAL_KS] [-c CUSTOM_SYSLINUX] \
[-i ISO] [-u ISO_URL] [-s SPLASH_IMAGE ] [--no-clean] DEVICE
```

This probably works for and on any RedHat based distro,
but has only been tested with CentOS 7.

This is pretty much just https://gist.github.com/pauljeff/4b9ad551cb6c35870d7c
turned into a script.

## License
MIT
