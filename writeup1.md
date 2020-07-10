#get ip network

ifconfig | grep inet #we get the address of our host and the mask which #tells us the addr of our network 192.168.1.0

#get ip all devices on the network
nmap -v -sn 192.168.1.0/24  | grep "is up" -B 1 

#scan for open ports 
nmap 192.168.1.35

#run dirb to see available urls
dirb 192.168.1.35

#access forum 
https://192.168.1.35/forum

http://192.168.1.35/forum/phpmyadmin forbidden
https://192.168.1.35/server-stats forbidden
