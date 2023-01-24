We can use the tree command to see the trees of directories\


`/bin` is a place used by the terminal commands such as ls, mount, rm, etc.

`/sbin` contains important administrative commands that should be only used by the superuser

`/lib` and `/lib64` directoriess contain files that are like the dlls of Windows

`/boot` contains files needed to start up the system, including the linux kernel, a RAM disk image and bootloader configuration files.

`/dev` contains all device files, which are not regular files but instead refer to various hardware devices on the system, including hard drives

`/etc` contains system-global configuration files, which affect the system behavior for all users.

`/home` contaisn the user's home directories\

`/media` is inteded as a mount point for external devises, such as hard drives or removable media

`/mnt` is also a place for mount points but dedicated to "temporarily mounted" devices, such as network filesystems.

`/opt` can be used to store additional software for a system that is not handled by the package manager.

`/proc` is a virtual filesystem that provides a mechanism for kernet to send information to processes.

`/usr` contains the majority of user utilities and applicaitons (it's like program file for windows), and partly replicates the root directory structure, containing for instance, among others, `/usr/bin` and `/usr/lib`

`/tmp` is a place for temporary files used by other applications.

`/var` is dedicated to variable data, such as logs, databases, websites, and temporary spool files that persist from one boot to another. A notable directory is the `/var/log` which contains the system log files
