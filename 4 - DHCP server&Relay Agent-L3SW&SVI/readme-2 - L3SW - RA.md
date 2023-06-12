
 
In this lab, we will be implementing DHCP server configuration with an L3 switch used as a DHCP relay agent (Another Router can be used as a relay agent too but I wanted to use L3 switch in this Lab folder so there will be no need to make another lab for SVI (instead of ROAS))


When we use SVI you will see that packets that will be sent within the LAN (Vlans) will not go to the router, they will be routed over the virtual interfaces of the L3 switch.

Vlan addresses and related ports are the same as the previous LAB in this folder. (But 30&40 will not be used)

The current LAB is already finished, when you want to do the configuration by yourself just Erase the NVRAM and restart like on the other labs.


Tips:
Create the pools  on the router with excluded addresses.
There will be no subinterfaces on the router, so just add an Ip address to the main interface. (Select a network address for the connection with the L3 switch. I used 192.168.1.2 for router and xxx1 for the switch)
The link between the switches is trunk. But some Cisco switches use Dot1q encapsulation on default some don’t (They use (ISL)— a Cisco proprietary protocol). So on the L3 side, you should add “sw tr encapsulation dot1q” and then continue the setup.
On the L3 sw do not forget to add ip routing (for intervlan and outside routing).
Create SVIs for related vlans. Add the default router IP address of the pools that will be created on the router to the related Vlan interface.
Add the ip helper addresses on the Vlan interfaces Closest Interface to the DHCP server)
The switch router connection will need an IP address – above given. Do not forget to add “no sw” in the interface.

video link: https://youtu.be/9qrXBQ4Is_M

