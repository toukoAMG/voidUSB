# voidUSB

Ever thought "I really want to make a persistent linux USB but I don't have the time"?

yeah me neither, anyway here is a script which might function or it might not, who knows (certainly not me).

Made to use as little dependencies as possible, all you need is a functioning linux system of any kind since the dependencies go as follows (the script will not run if all dependencies cannot be found):

```
util-linux (for sfdisk)
bash (don't know if pure sh or others work, zsh probably will though)
dosfstools (to make EFI system partition)
e2fsprogs (ext4 boot partition)
f2fs-tools (for the USB oriented f2fs filesystem)
curl
tar
xz
```
## Installation/Usage
### From stable release
Navigate to the [releases page](https://notabug.org/toukoAMG/voidUSB/releases), and download the source code. Then extract it and edit the config file before running the script. For example:
```
wget https://notabug.org/toukoAMG/voidUSB/archive/v1.0-rc1.tar.gz
tar xf v1.0-rc1.tar.gz
cd voidusb
vim voidusb.conf
./voidusb
```
### From git (more recent but potentially less stable)
It's as simple as running a few commands (and editing a configuration file):
```
git clone --branch stable https://github.com/rangerAMG/voidUSB.git && cd voidUSB # or keep on master by removing the --branch stable , however you likely will encounter issues if you do that
vim voidusb.conf # or use your text editor of choice, gedit/kate is normally good for newbies
./voidusb
```
Or to run just one function (depchecker, usbchk, partition, mountusb, tarstrap, xbpsstrap, prepchroot, tarchroot, localisation, bootloader, mkfstab, shell, usercreation, drivers, gui):
```
./voidusb run FUNCTION
```

## To do list:
* Add advanced customisation options
* !!DONE!! ~~Add option to install via XBPS for distros that have XBPS available~~
* A fully portable version (Option could be toggled via command line flags)
* Different filesystem and maybe OS support (Artix and Gentoo anyone?)
* !!DONE!! ~~Add an option to install a GUI (I would prefer lightdm and budgie-desktop)~~
* !!DONE!! ~~Launch the separate functions with ./voidusb run mkfstab~~
