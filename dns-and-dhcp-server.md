

1. We update references `apt-get update`

2. We can search available apps using `apt-cache search name (for example dnsmasq)`

3. Install dnsmaq `apt-get dnsmasq`

To enable DNS

4. Edit the settings `sudo nano /etc/dnsmasq.conf`

We enable `domain-needed` to never forward plain names and enable `bogus-priv` to never forward addresses in the non-routed address spaces

We can add local domains by modifying:

`local=/domainname.com/` 

Note that these queries are not forwarded to the internet / only answered to dhcp clients

We can add addresses such as:

`address=/r1/10.1.1.1`
`address=/docker2/10.1.1.100`


5. Then we restart the dns server `systemctl restart dnsmasq`

To enable DHCP

1. Edit the settings `sudo nano /etc/dnsmasq.conf`

such as adding dhcp ranges `dhcp-range lowerrange, upperrange, leasetime`

`dhcp-range=10.1.1.150, 10.1.1.199, 24h`

2. Set DHCP Options

For example `dhcp-options=3,10.1.1.1` would point as the DNS server the device on that IP

3. restart the dns server `systemctl restart dnsmasq`

Note: we can shut down interfaces in linux using: `sudo ip link set interfacename_(example ens3) down

We can check dns leases using:

`cat /var/lib/misc/dnsmasq.leases`