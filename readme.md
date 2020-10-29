This is the documentation for my Router appliance on a linux ubuntu system.
This contains the relevent configs for my main services, these include:
- dns
- dhcp
- fw 
- squid

See relevent folders to find the specific config files to be placed within each repository. 

DNS:
We used BIND9 DNS to do the DNS services use the following commands in sequence to install BIND9

sudo su
apt-get install bind9

The service is installed and running at this time. From there you can change the conf file to the one provided in this repository and restart the service.

DHCP:
Used the regular DHCP with the ubuntu distro packages, Install with the following commands:

sudo apt-get install isc-dhcp-server

Navigate to the config files transfer provided configurations and restart service with 
sudo service isc-dhcp-server restart

FW:
Using UFW for the main firewall all that is needed is to turn on UFW with the command:

sudo ufw enable

Followed by loading configuration and then restarting the service. 

Squid:
Using squid for proxy service, install the relevent service with these commands:

sudo apt install squid

Load configuration provided and restart the service.

This should restore the majority of all services. 