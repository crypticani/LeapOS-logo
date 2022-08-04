# plymouth-theme-LeapOS-logo
Portrait mode (rotated monitor) for Kubuntu start-up and shut-down logo.

This is a `plymouth` theme for LeapOS (Ubuntu with the KDE package `kubuntu-desktop` installed), that will display the default logo at start-up and shutdown, for a rotated monitor.

The images are rotated 90 degrees counter-clockwise, meaning that you have rotated your monitor 90 degrees clock-wise. For the other direction, all image files in the `images/` subdirectory will have to the rotated again in the other direction, using some image processing tool (I used gimp for this purpose).

This is _**incomplete**_ and only the logo images are rotated, meaning the other user interface elements like a password prompt during boot have not been tested and will likely not work as intended. Rotate for text lines is not tested also and will likely show the text line clipped at a size of a few characters.

This theme is a copy of the default kubuntu theme from package `plymouth-theme-kubuntu-logo`, with the logo of LeapOS.
# Installation
Clone or copy the repository contents at the following directory:
```
cd /usr/share/plymouth/themes/

git clone https://github.com/crypticani/LeapOS-logo.git
```
  
Next, run the following commands:

```
    update-alternatives --install \
        /usr/share/plymouth/themes/default.plymouth \
        default.plymouth \
        /usr/share/plymouth/themes/LeapOS-logo/LeapOS-logo.plymouth \
        210 \
          --slave \
            /usr/share/plymouth/themes/default.grub \
            default.plymouth.grub \
            /usr/share/plymouth/themes/LeapOS-logo/LeapOS-logo.grub
```

```
update-initramfs -u
```
