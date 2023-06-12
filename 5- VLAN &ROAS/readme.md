In this lab, we will be implementing the VLAN and ROAS concepts.

The lab is already finished; you can check the device configurations and perform ping tests to observe it in simulation mode. Edit the simulation tab to allow only ICMP messages in the IPv4 tab to ensure that other messages are prevented from being seen.
For testing, you can check your IP address from the command prompt of the PCs (C:>ipconfig /all).

If you want to start from the beginning, simply erase the NVRAM in the config tab of the devices and restart them all using the "reload" command.

Your tasks:
You need to create the necessary VLANs on switches and arrange ports according to the given information below:
The switch name corresponds to the VLANs it currently has.
VLAN10-20-40: f0/1-10 is VLAN10, f0/11-20 is VLAN20, f0/21-24 is VLAN40.
The same coding is used on the switches.

PC names: I have already connected the PCs to f0/1, f0/11, and f0/21 ports of the switches. You should add the related IP addresses according to the network address of the VLANs or setup a DHCP server on the main router.

You should set your links between the switches as trunk ports and allow the necessary VLANs on them.
For example, the g0/2 trunk port between the last two switches should only allow VLAN10 and VLAN30, since there are no PCs in the last switch related to VLAN20 and VLAN40.

Later, configure subinterfaces on g0/2 of the main router for VLAN routing.
The network addresses for the VLANs are provided in the lab and topology picture (e.g., VLAN20 is 10.0.20.0/24).

Once everything is set up, you should be able to ping every PC in different VLANs. However, please verify this in simulation mode, as packets will be going through the router first.

Since all subinterfaces on the main router can already communicate with each other (you can check with the "show ip route" command), you do not need to define any routing. But if you need to ping the router at 10.0.0.1, you will need to define a route for all the VLANs under the R_out. (No additional configuration is needed on the main router, as it is already connected to 10.0.0.1 via g0/0.)

video link: https://youtu.be/NZL4kI776RM




