# Building-An-Organization-VPN-Network
## Objective
Design and implement a virtual VPN network infrastructure on Packet Tracer to securely connect multiple remote locations and facilitate seamless communication between them while ensuring confidentiality, integrity, and availability of data transmission, and at the same time gaining indepth understanding of basic network protocols.
### Skills Learned
- Advanced comprehension of IP addressing, routing protocols, switching mechanisms, and VLAN configuration.
- Advanced understanding of basic network configuration. 
- Enhanced knowledge of network protocols. 
- Development of critical thinking and problem-solving skills in cybersecurity and networking.

### Tools Used
- Packet Tracer.
- Google (for research) .
## Steps
## Step 1 Network Design :
This network design framework offers a systematic approach to architecting, addressing, routing, and securing the organization's network, guaranteeing a resilient and adaptable infrastructure that can be expanded to meet future growth.
The network design diagram helps to give a clear idea of what the network infrastructure should look, and which the network device is connected to which device. since this project was a simulation, only few network devices were used , as shown in the image below

![Alt Network Diagram ](https://github.com/Adegbenga-111/Building-An-Organization-VPN-Network-/blob/main/to%20be%20used%20as%20the%20network%20diagram.png)
*image 1: Network Diagram*
## Step 2 Router Configuration :
According to image 1 , there are three routers which are 192.168.1.1, ISP, 10.0.1.1. In order to create this network each of the router as to be configured using the cisco CLI(command line interface).
Router 192.168.1.1 Configuration:
 - Router>enable
 - Router#config t

**This lines of command is to move from User Exec mode to Global Configuration mode(All configuration are done in this mode) .**

-  Router(config)#int fa0/0
-  Router(config-if)#ip add 192.168.1.1 255.255.255.0 
-  Router(config-if)#no shut

 **This lines of command is to configure fast/ethernet0/0 for 192.168.1.1, as shown in the image below.**
 ![Alt fast/ethernet0/0 for 192.168.1.1 ](https://github.com/Adegbenga-111/Building-An-Organization-VPN-Network-/blob/main/projecy/192.168.1.%204_27_2024%203_52_59%20PM.png)
*image 2: fast/ethernet0/0 for 192.168.1.1 *
-   Router(config-if)#exit
-   Router(config)#int fa0/1
-   Router(config-if)#ip address 13.2.5.3 255.0.0.0
-   Router(config-if)#no shut

  **This lines of command is to configure fast/ethernet0/1 for 192.168.1.1 , as shown in the image below.**
   ![Alt fast/ethernet0/1 for 192.168.1.1 ](https://github.com/Adegbenga-111/Building-An-Organization-VPN-Network-/blob/main/projecy/192.168.1.%204_27_2024%203_52_53%20PM.png)
*image 3: fast/ethernet0/1 for 192.168.1.1 *
Router ISP Configuration:
-Router>enable
-Router#config t

**This lines of command is to move from User Exec mode to Global Configuration mode(All configuration are done in this mode) .**

- Router(config)#int fa0/0
- Router (config-if)#ip add 12.2.5.3 255.0.0.0
- Router(config-if)#no shut
- Router(config-if)#exit

 **This lines of command is to configure fast/ethernet0/0 for ISP , as shown in the image below.**
![Alt configure fast/ethernet0/0 for ISP](https://github.com/Adegbenga-111/Building-An-Organization-VPN-Network-/blob/main/projecy/ISP%20(13.2.5.7)%20(12.2.5.3)%204_27_2024%203_53_22%20PM.png)
*image 4: fast/ethernet0/0 for ISP*
- Router(config)#int fa0/1
- Router(config-if)#ip add 2.0.0.1 255.0.0.0
- Router(config-if)#no shut

 **This lines of command is to configure fast/ethernet0/1 for ISP , as shown in the image below.**
 ![Alt  configure fast/ethernet0/1 for ISP ](https://github.com/Adegbenga-111/Building-An-Organization-VPN-Network-/blob/main/projecy/ISP%20(13.2.5.7)%20(12.2.5.3)%204_27_2024%203_53_29%20PM.png)
*image 5: fast/ethernet0/1 for ISP*
