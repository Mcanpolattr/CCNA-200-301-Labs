
 
In this lab implemented STP & HSRP synchronization, together with DHCP servers applied on redundant rooters, applied ether channels between leftover switch links for loadbalance, used OSPF in routing, and check the connectivity by cutting different lines for simulation and to be sure that DHCP clients can still get their IP addresses from the other router. Applied basic security rules. 

When you start the lab you can connect the PCs given below to the AS switches. 
AS switch ports 1-8 are reserved for VLAN10, 9-16 are for VLAN20.
DS1 is the root bridge for the VLAN10, and DS2 is the root for VLAN20. And also they are the secondary roots for the other VLAN.
And again RV10 is the active rooter for VLAN10, and standby by for the VLAN20. RV20 is the opposite.
By doing so we are directing the messages coming from VLAN10 to DS1 and RV10, and messages from VLAN20 are directed to DS2 and RV20 first.
ROAS is used for VLAN routing (because I used L2 switches as DS). (* May be in the next LAB I can use L3 switches with DHCP relay agent.)
We also make both rooters DHCP servers for VLAN10 and VLAN20. (Their Original IP addresses are x.x.x.1 and their Virtual IP addresses are x.x.x.10) and x.x.x.1 to x.x.x.10 are excluded addresses for DHCP pools

Links between the switches are used for ether channels. You can use any type you desire (I have used Cisco’s PAgP)

And as a last OSPF used for routing

For testing: You can use ipconfig /renew in simulation mode to see, from which rooter they have taken the IP addresses. (To do so I suggest closing everything on the filer only leaving DHCP on edit tab for simulation, or else everything gets messy.)

Used IP address ranges, port numbers, bundled ports for etherchannel, router IDs are given in the picture and lab.
If you want to do this by yourself from the beginning, just erase the NVRAM at the config tab of the devices and reload them all.


