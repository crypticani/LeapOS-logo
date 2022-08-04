# plymouth-theme-LeapOS-logo
Plymouth theme for LeapOS.

This is a `plymouth` theme for LeapOS (Ubuntu with the KDE package `kubuntu-desktop` installed), that will display the LeapOS logo at start-up and shutdown.

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
