# CONFIGURING ACME #

Acme.exe is the same (mostly) as the inferno-os emu(1), so the command line arguments are the same (except for -I, see below). Acme.exe reads the EMU environment variable for options first, then processes the command line options.

If no dis command is given on the command line to Acme.exe then the default command is 'sh -l', see sh(1). The -l option will cause the shell to run as a login shell, which means it first runs the file /lib/sh/profile, and then ./lib/profile if that file exists.

/lib/sh/profile is mostly concerned with making sure a home directory exists for the current user, then changing to that directory, so the ./lib/profile in that users directory will be run, i.e. /usr/yourname/lib/profile.

It is your $home/lib/profile where most of the action is. It sets up various things, namespace, factotum, environment variables (e.g. for fonts), and finally it launches acme.

If you want to change the arguments that start the actual acme editor then edit your $home/lib/profile.

If you want to change the command line arguments the Acme.exe, the emulator, then either modify EMU environment var, or on Nt create a shortcut, modify its properties changing the command line with the options you want.

Also, edit $home/lib/profile if you want to add more things to your namespace at startup.

# acme.exe vs. emu.exe #

Emu.exe is built as a console application whereas acme.exe is built as a windows application. Therefore -I, which disables stdin/stdout for emu.exe has the opposite meaning for acme.exe, i.e. console stdin/stdout is disabled by default in acme.exe. But because it is a windows application even if you enable it, it still won't work; you'd need to rebuild acme.exe as a console application (an instance is on the downloads page).

Acme.exe uses the current directory as the default root of the inferno tree; emu.exe uses /usr/inferno.

Acme.exe starts the first shell as a login shell, emu.exe doesn't.