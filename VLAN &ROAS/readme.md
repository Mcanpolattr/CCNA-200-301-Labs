
 
In this lab we will be implementing the VLAN and ROAS concepts.

The lab is already finished; you can check the device configs and do the ping tests to see it in simulation mode. Edit sim. tab to only allow the ICMP messages at the IPV4 tab to be sure that prevent other messages seen.
For testing you can check your IP address from the command prompt of the PCs (C:\>ipconfig /all)


If you want to do this by yourself from the beginning, just erase the NVRAM at the config tab of the devices and restart (reload command) them all.
Your Tasks:
You need to create the necessary VLANs on switches and arrange ports according to the given information below:
Switch name is referred to as the present VLANs it has.
VLAN10-20-40: f0/1-10 is VLAN10, f0/11-20 is VLAN20c, f0/21-24 is VLAN40.
The same coding on the switches are used.
PC names: I already connected the PCs to f0/1, 11 and 21 ports of the switches. You should add the related IP addresses according to the network address of the VLANs. Default router address will be x.x.x.1.(I already arranged PCs to have automatic Ip addressing from DHCP server, and if you want to only use this part (to get awy setting all IP addresses manually: After erasing NVram, load startup config to the main router form attached .txt file and restart)

You should set your links between the switches as trunk ports and allow the necessary VLANs to it.
Ie: The g0/2 trunk port between the last 2 switches should only allow Vlan10 and 30. Because there no PCs in the last Switch related to VLAN 20 and 40. 

Later arrange the Subinterfaces on g0/2 of the main router for VLAN routing.
Network addresses for the VLANs are on the lab and topology picture (ie: Vlan20 is 10.0.20.0/24)

When all is finished you should be able to ping every PC in different VLANs, but check that in simulation; packets will be going over the Router first. 

Because all subinterfaces on the main router is already can see each other (you can check show ip route), you do not need to define any routing. But If you need to ping 10.0.0.1 router, you need to define a route for all the VLANs under the main router. (On the main router you do not need to do anything because 10.0.0.1 is connected to g0/0 already)
