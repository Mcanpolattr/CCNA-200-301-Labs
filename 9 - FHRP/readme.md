In this lab, we will be implementing FHRP.

We will using Cisco’s HSRP (Hot Standby Router P.)

You can use version 2 in your settings. (This supports IPv6 addresses and allows more groups to be configured although here we will use only VLan1)

You can check the topology for details.

Testing: You can cut the links going to the active router to see that pings send by PCs to reach 3.3.3.3 will be going over through the standby router. (use tracert to check the next hops)




