`less /etc/passwd` -> list of users
`ps aux | less` -> list of processes running

On files list ( `ls -l` ) for example: root root would mean that the user owner is root and the group owner is also root.

Different processes use different service accounts.

For example for dns services, it uses the "dnsmasq" accounts, or the sshd service would use the sshd account.

Form example:

sshd:x:110:65534::var/run/sshd:/usr/sbin/nologin

would mean that `var/run/sshd:` is the home directory for this user and `/usr/sbin/nologin` means that no user can initiate a shell with that account 

Note: If we only remember part of a command, we can just type what we remember and double tab, it should show the options we could type.

`useradd -help` allows us to see the options to manipulte users.

if we type `id X` while the X is the username, we can see the user id, group id and group it belongs.

If we wanted to add shell use to an user, we can: `usermod james -s /bin/bash`, we probably also need to add or create his home directory.

`sudo passwd james` would allows us to change his password

`groups` -> show us all created groups`

`groupadd --help` -> shows the options

`groupadd sales` -> creates a group called sales`

`cat /etc/group | grep sales` -> filtering for the sales group

`usermod -aG sales james` -> appends James to the sales group (without the a parameter, it would overwrite the groups of james)

`passwd --help` allows us to see options related to locking users, and passwords, for example, a locked user can't log in.

An ! after the double colons on `grep username etc/shadow` means that the user is locked

`chage username` allows us to set many password attributes for a password

If we wanted to edit the default password attributes of everyone, we can edit the `/etc/login.defs` files 