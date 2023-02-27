Taking as example tftpd-hpa for Ubuntu:

1. Install using  `sudo apt-get install tftpd-hpa.`

2. Configure to allow uploading:

`nano /etc/default/tftpd-hpa`

and we edit the line 

`TFTP_OPTIONS="--secure"` to `TFTP_OPTIONS="--secure --create"`

3. By default, the files are stored in `/var/lib/tftpboot` and have as owner the root account

We have to run the `sudo chown -R tftp /var/lib/tftpboot` to change the ownership to the tftp user

4. Restart for changes to take effect

`sudo service tftpd-hpa restart`

