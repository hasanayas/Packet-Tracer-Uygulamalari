
![Ağ Toplojisi-2](https://user-images.githubusercontent.com/86951716/157085606-ec62f4a3-2a64-4b7a-a379-2a0bc656b406.png)

# Yönlendirme Komutları- Router A
- Router(config)#hostname A
- A(config)#int fa0/0
  - A(config-if)#ip address 192.168.1.1 255.255.255.0
  - A(config-if)#no sh

- A(config-if)#int e0/0/0
  - A(config-if)#ip add 192.168.100.1 255.255.255.252
  - A(config-if)#no sh

- A(config-if)#int fa0/1
  - A(config-if)#ip add 192.168.100.5 255.255.255.252
  - A(config-if)#no sh


# Yönlendirme Komutları- Router B
- Router(config)#hostname B
- B(config)#int fa0/0
  - B(config-if)#ip address 192.168.2.1 255.255.255.0
  - B(config-if)#no sh

- B(config-if)#int fa0/1
  - B(config-if)#ip address 192.168.100.2 255.255.255.252
  - B(config-if)#no sh


# Yönlendirme Komutları- Router C
-Router(config)#hostname C
- C(config)#int fa0/0
  - C(config-if)#ip add 192.168.3.1 255.255.255.0
  - C(config-if)#no sh

- C(config-if)#int fa0/1
  - C(config-if)#ip add 192.168.100.6 255.255.255.252
  - C(config-if)#no sh


# Statik Yönlendirme Komutları- Router A
- A(config)#ip route 192.168.2.0 255.255.255.0 192.168.100.2
- A(config)#ip route 192.168.3.0 255.255.255.0 192.168.100.6

# Statik Yönlendirme Komutları- Router B

- B(config)#ip route 192.168.1.0 255.255.255.0 192.168.100.1
- B(config)#ip route 192.168.100.4 255.255.255.252 192.168.100.1
- B(config)#ip route 192.168.3.0 255.255.255.0 192.168.100.1

# Statik Yönlendirme Komutları- Router C
- C(config)#ip route 192.168.1.0 255.255.255.0 192.168.100.5
- C(config)#ip route 192.168.2.0 255.255.255.0 192.168.100.5
- C(config)#ip route 192.168.100.0 255.255.255.252 192.168.100.5
