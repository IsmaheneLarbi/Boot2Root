#get ip network

ifconfig | grep inet #we get the address of our host and the mask which #tells us the addr of our network 192.168.1.0

#get ip all devices on the network
nmap -v -sn 192.168.1.0/24  | grep "is up" -B 1 
