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

==> DIRECTORY: https://192.168.1.35/forum/                                     
==> DIRECTORY: https://192.168.1.35/phpmyadmin/                                
+ https://192.168.1.35/server-status (CODE:403|SIZE:294)                       
==> DIRECTORY: https://192.168.1.35/webmail/  

http://192.168.1.35/forum/phpmyadmin forbidden
http://192.168.1.35/server-status forbidden




in the logs posted by lmezard there's an error caused by a login attempt with an invalid username !q\]Ej?*5K5cy*AJ . This login attempt is followed by a successful login by lmezard. Given the fact that the invalid login looked like a passszord, we wonder if lmezard mistakenly gave his password and decide to check.
now that we have mail/pwd we use it to connect on squirrelmail

we find a mail giving us access to the database using root/Fg-'kKXBj87E:aJ$

laurie's email is stored as 0171e7dbcbf4bd21a732fa859ea98a2950b4f8aa1e5365dc90

