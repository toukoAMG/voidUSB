# voidUSB

Ever thought "I really want to make a persistent linux USB but I don't have the time"?

yeah me neither, anyway here is a script which might function or it might not, who knows (certainly not me).

Made to use as little dependencies as possible, all you need is a functioning linux system of any kind since the dependencies go as follows:

```
util-linux (for sfdisk)
bash (don't know if pure sh or others work, zsh probably will though)
dosfstools (to make EFI system partition)
e2fsprogs (ext4 boot partition)
f2fs-tools (for the USB oriented f2fs filesystem)
curl
tar
```

## To do list:
* Add advanced customisation options
* Add option to install via XBPS for distros that have XBPS available
* A fully portable version (Option could be toggled via command line flags)
* Different filesystem and maybe OS support (Artix and Gentoo anyone?)
