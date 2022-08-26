# shared-mime-info-patch
RPM-patch for displaying VirtualBox disk icons

To the already known [problems with the display of mime-type icons](https://gitlab.gnome.org/GNOME/nautilus/-/issues/2190) (files with various extensions) with the release of the update `shared-mime-info-v2.2` one problem has become more. Now in Mageia-9 and probably in other distributions, virtual machine disk icons are no longer displayed: `*.vdi, *.vhd, *.vmdk, *.ova`.

The problem is related to the inclusion of the description of these mime types in the source file `/usr/share/mime/packages/freedesktop.org.xml`. As practice has shown, it takes years to wait for corrections. If you need to fix the problem right now, you can install the package `shared-mime-info-patch`. After installation, it automatically applies the patch specified below and starts updating the database: `update-mime-database /usr/share/mime`. If the package is deleted, the change will be rolled back to the original.

Issue: https://gitlab.freedesktop.org/xdg/shared-mime-info/-/issues/188

**Similar programs:** [adwaita-mime-patch](https://github.com/AKotov-dev/adwaita-mime-patch)

Icons before the patch:

![](https://github.com/AKotov-dev/shared-mime-info-patch/blob/main/ScreenShots/before-patch.png)

Icons after the patch:

![](https://github.com/AKotov-dev/shared-mime-info-patch/blob/main/ScreenShots/after-patch.png)
