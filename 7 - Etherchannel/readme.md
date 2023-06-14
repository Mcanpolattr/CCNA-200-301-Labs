In this lab, we will be implementing EtherChannel.

Normally, when we make two connections between the same switches, due to STP, one will be in the blocking mode, and in case the other one fails, it will transition to the forwarding state.

With EtherChannel, we can bundle up to eight ports to act as one whole link between the switches.

There are three versions:

PAgP (Port Aggregation Protocol)
a. Cisco proprietary protocol
b. Dynamic
LACP (Link Aggregation Control Protocol)
a. IEEE 802.3ad
b. Dynamic
c. Works on all switches
Static EtherChannel
Not dynamic
No protocol is used; defective ports will be taken off.

The current lab is already finished. You can check the Portchannels by using the command "sh ether sum" (short for show ether summary). When you want to configure it yourself, just erase the NVRAM and restart, as you would in the other labs.

By looking at the topology, you can determine which ports need to be bundled and in which mode.

Wording:xxxx

[auto & desirable] = PAgP (similar to DTP) -- Auto & Auto - No EtherChannel; other forms EtherChannel (one desirable is enough)

[active & passive] = LACP; having one active is sufficient

[on] = Static - both should be on