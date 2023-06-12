
 
In this lab we will be implementing DHCP server configuration, for 4 Pools (VLan) – Current LABs are already finished, when you want to do the configuration by yourself just Erase the NVRAM and restart like on the other labs.

I noticed that when I use DHCP servers in the labs it makes everything much easier for the endpoints. (You just select the PCxx/config/interface and select DHCP / instead of adding IP addresses and Default router manually). And anyway in our usual life we are mostly using DHCP on our laptops/PCs etc.

In the first Lab, we will have 2 routers that will be used as DHCP servers for VLan10&20 and VLan30&40 respectively. (Excluded addresses are the first 1-10 adresses)

Network addresses for the Vlans are given, and on the switch, ports setup is like below (You can understand which PC is belong to which Vlan and they are connected to related ports below)
F0/1-5 : VLAN10
F0/6-10 : VLAN20
F0/11-15 : VLAN30
F0/16-20 : VLAN40

After you set your routers and the switch, you can use ipconfig /renew on the PCs to get the IP addresses automatically.

PS!!: In the simulation, if you do ping tests you will see that VLAN10&20 can ping each other but can not ping VLAN30&40. If you want to ping the other VLANs on the other router, you should create one on the router, related subnet interfaces, and also on the switch uplinks should add the switch VLANs you want to reach to the allowed trunk.


Tips:
First arrange the ports on the switch.
Then create the trunk Vlans on the uplinks, going to the related router.
On the routers you should make ROAS for 2 sub interfaces.
Create the DHCP pools, you can add DNS server if you want, don’t forget to add excluded addresses.

video link: https://www.youtube.com/watch?v=xhFWTcyDVJo
