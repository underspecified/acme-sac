# Introduction #
This page describes how to build the Debian package of acme-sac.


# Details #

You can start by downloading the latest Debian package from the downloads to view the directory hierarchy:
```
  root/
    DEBIAN/control
    usr/bin/acme
    usr/share/acme-sac
    usr/share/applications/acme-sac.desktop
```


To extract the downloaded .deb file `dpkg-deb -R file.deb`.
  * Replace the **usr/share/acme-sac** folder with the latest from mercurial.
  * Replace **usr/bin/acme** with the latest emu build from acme-sac.
  * Update the version number in **DEBIAN/control**

Build the package, install it and test it.
```
  $ dpkg-deb -b root-folder acme-sac_0.15_i386.deb
  $ sudo dpkg -i acme-sac_0.15_i386.deb
  $ acme
```