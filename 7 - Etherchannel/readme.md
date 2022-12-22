In this lab, we will be implementing Etherchannel.

Normally when we make 2 connections between the same switches, because of STP one will be waiting int the block mode, in case of the other one fails it will go on to forwarding state.

With Etherchannel, we can bundle up to 8 ports to act as one whole link between the ports. 

There are 3 versions:

1. PAgP (Port Aggregation Protocol)
	a. Cisco proprietary protocol
	b. Dynamic
2. LACP (Link Aggregation Control Protocol
	a. IEEE 802.3ad
	b. Dynamic
	c. Works on all SW 
3. Static EtherChannel
	1. Not dynamic
	2. There is no protocol is used defected ports will be taken off. 


The current LAB is already finished, you check the Portchannels by “sh ether sum” (in short) when you want to do the configuration by yourself just Erase the NVRAM and restart like on the other labs.

By looking at the topology you can see which ports need to be bundled in which mode.





