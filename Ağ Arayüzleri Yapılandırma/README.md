# Router Komutları 

- Router(config)# interface f0/0
- Router(config-if)#ip address 192.168.1.1 255.255.255.0
- Router(config-if)#no shutdown 
- Router(config-if)#description left-network

- Router(config-if)#exit

- Router(config)#interface f0/1
- Router(config-if)#ip address 192.168.2.1 255.255.255.0
- Router(config-if)#no shutdown 
- Router(config-if)#description right-network

- Router#copy running-config tftp: 
- Address or name of remote host []? 192.168.1.100
- Destination filename [Router-confg]? backup-07032022
