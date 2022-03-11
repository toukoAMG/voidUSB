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
It's as simple as running a few commands (and editing a configuration file):
```
git clone https://notabug.org/rangerAMG/voidUSB.git && cd voidUSB
vim voidusb.conf # or use your text editor of choice, gedit/kate is normally good for newbies
./voidusb
```

## To do list:
* Add advanced customisation options
* Add option to install via XBPS for distros that have XBPS available
* A fully portable version (Option could be toggled via command line flags)
* Different filesystem and maybe OS support (Artix and Gentoo anyone?)
* Add an option to install a GUI (I would prefer lightdm and budgie-desktop)
* Launch the separate functions with ./voidusb run mkfstab