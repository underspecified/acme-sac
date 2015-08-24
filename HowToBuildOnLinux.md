# Introduction #

Here are instructions on how to build Acme-SAC on Linux. This assumes no currently working Acme-SAC on the host, otherwise you can build inside Acme-SAC using mk.

# Details #

Starting with a brand new Xubuntu install, open terminal and type the following:
```
  $ sudo apt-get install libx11-dev
  $ sudo apt-get install libxext-dev
  $ sudo apt-get install mercurial
  $ hg clone https://code.google.com/p/acme-sac
  $ cd acme-sac/sys
  $ ./build.sh
  $ cd ..
  $ cp sys/emu/Linux/o.emu emu

```

Once you have emu in your root of the acme-sac directory, you can type ./emu to launch Acme-SAC.
