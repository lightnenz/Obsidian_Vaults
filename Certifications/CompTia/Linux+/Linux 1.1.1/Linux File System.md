# Linux File System

- A **Directory** is the correct term for a container with file insie. Folders is often used synonymously with the term **directory**.
- Everything in a Linux distro is a file of some kind.

- **/home** - This is a user's home directory and where all for the user's filer are stored.
- **/root** - This is the root user's home directory .
- **/boot** - This is where the boot loader and the kernel files are stored.
- **/etc** - Text config for installed applications and the system are stored here.
- **/opt** - This is for add-on packages.
- **/media** - This is where removable media is mounted, like **USB**.
- **/mnt** - This is where temp mounted file systems go.
- **/tmp** - This is where temp files go. It is usually deleted on reboot
- **/sbin** - Essential binary files.
- **/bin** - Essential binaries that aren't system specific such **/bin/bash**
- **/lib** - System Library files for **/sbin** and **/bin**
- **/usr** - Things not needed for single user mode
- **/var** - This is where files that tend to change a lot go such as logs an emails
- **/dev** - This is hardware represented as a file. This can be things such as hard drives, com ports, sound cards etc
- **/proc** - This is process information that is generated don the fly, it is also used for some kernel info
- **/sys** - info about devices, drivers and kernel info