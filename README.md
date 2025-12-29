# Building

* Install [_devkitARM_](https://devkitpro.org/wiki/Getting_Started). See also
  https://gbadev.net/tonc/setup.html#sec-dkp and https://devkitpro.org/wiki/devkitPro_pacman.
* Set required paths for _devkitARM_ and build _Goomba Color_, for instance
  `DEVKITPRO=/opt/devkitpro DEVKITARM=/opt/devkitpro/devkitARM make`.

## Mini how-to to install _devkitARM_ for Debian

_devkitPro_ provides packages for the package manager _Pacman_, which is native to _Arch Linux_ and
also used by _MSYS_ (Windows tooling). For Debian they provide an _Apt_ repository for a self
contained _Pacman_ installation.
Using that, you are able to finally install packages `devkitARM` and `gba-dev`.

Rough steps:
* Add _Apt_ repository https://apt.devkitpro.org including GnuPG key. See [script
  `install-devkitpro-pacman`](https://apt.devkitpro.org/install-devkitpro-pacman).
* Run `apt update`.
* Install `apt install devkitpro-pacman`.
* Update _Pacman_ packages with `dkp-pacman -Sy`.
* Install final packages with `dkp-pacman -S devkitARM gba-dev`.
