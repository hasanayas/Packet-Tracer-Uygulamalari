# Ağ Topolojisi


![Ağ Topolojisi-2](https://user-images.githubusercontent.com/86951716/158167413-e9c6ad10-9ce3-4468-a252-ee73ff3429b1.png)

<br/>

# Yeni Genel Yayın Bölgesi Oluşturulduktan Sonra Router Komutları

- C(config)#interface e0/0/0
  - C(config-if)#ip add 192.168.100.10 255.255.255.252<br/>
- B(config)#interface e0/0/0
  - B(config-if)#ip add 192.168.100.9 255.255.255.252<br/>

A(config)#ip route 192.168.2.0 255.255.255.0 192.168.100.6 <br/>
A(config)#ip route 192.168.3.0 255.255.255.0 192.168.100.2 <br/>

B(config)#ip route 192.168.1.0 255.255.255.0 192.168.100.10 <br/>
B(config)#ip route 192.168.3.0 255.255.255.0 192.168.100.10 <br/>

C(config)#ip route 192.168.1.0 255.255.255.0 192.168.100.9 <br/>
C(config)#ip route 192.168.2.0 255.255.255.0 192.168.100.9 <br/> 

![2](https://user-images.githubusercontent.com/86951716/158845821-8fb70154-c3a4-4da0-9a1c-4c61341fb5e2.gif)



# Maliyete Göre Yönlendirme Router Komutları 

- A(config)#no ip route 192.168.2.0 255.255.255.0 192.168.100.6 
- A(config)#ip route 192.168.2.0 255.255.255.0 192.168.100.6 2
- A(config)#no ip route 192.168.3.0 255.255.255.0 192.168.100.2
- A(config)#ip route 192.168.3.0 255.255.255.0 192.168.100.2 2  <br/>  <br/>    

- B(config)#no ip route 192.168.1.0 255.255.255.0 192.168.100.10
- B(config)#ip route 192.168.1.0 255.255.255.0 192.168.100.10 2
- B(config)#no ip route 192.168.3.0 255.255.255.0 192.168.100.1
- B(config)#ip route 192.168.3.0 255.255.255.0 192.168.100.1 2 <br/> <br/>

- C(config)#no ip route 192.168.1.0 255.255.255.0 192.168.100.9
- C(config)#ip route 192.168.1.0 255.255.255.0 192.168.100.9 2
- C(config)#no ip route 192.168.2.0 255.255.255.0 192.168.100.5
- C(config)#ip route 192.168.2.0 255.255.255.0 192.168.100.5 2 <br/>



![1](https://user-images.githubusercontent.com/86951716/158845998-3fe54efa-f8b3-41a5-aeb9-4d2d353e7fa6.gif)

![3](https://user-images.githubusercontent.com/86951716/158845081-11747745-69e5-4ab3-af74-62374b8b5379.gif)



