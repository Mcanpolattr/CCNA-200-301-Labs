In this lab, we will be implementing FHRP.

We will using Cisco’s HSRP (Hot Standby Router P.)

You can use version 2 in your settings. (This supports IPv6 addresses and allows more groups to be configured although here we will use only VLan1)

You can check the topology for details.
We will use the shared virtual IP for default router as 10.0.0.10/24. This is already set on the PCs. WE also added the IP of the PCs as .11 and 12.

Testing: You can cut the links going to the active router to see that pings send by PCs to reach 3.3.3.3 will be going over through the standby router. (use tracert to check the next hops)
We will also demonstrate how the "preempt" command is taking effect.

Video link: https://youtu.be/UeDFTbR-x2g







