# Introduction #

The following instructions describe how to compile the Dis emulator executable to run Acme-SAC on Windows.


# Details #

Follow these steps to compile on Windows:
  * Install the latest Windows SDK
  * Open the Windows SDK command prompt, which will be in the SDK program group in the Start menu.
  * Set the environment inside the command prompt using the **setenv** cmd. See setenv /? for options. This is what I use: `setenv /Release /x86 /win7`
  * Launch the acme.exe from inside the command prompt: `D:\acme-sac\acme.exe`
  * Inside acme-sac open a command shell using **win**
  * Inside win execute the commands below:
```
  % cd /sys
  % run Nt/profile
  % mk install
```