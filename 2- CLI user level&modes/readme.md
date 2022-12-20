https://www.cisco.com/E-Learning/bulk/public/tac/cim/cib/using_cisco_ios_software/02_cisco_ios_hierarchy.htm
This hierarchy level of CLI modes is taken from the above site.

It helps you to understand which mode you are in by checking the cursor on the left.
It also gives some samples of commands that can be used in those lines.
Here below are some commands that you will use in the following labs
Switch>enable  (get into user exec mode)
Switch#show running-config (shows whole running	config)
Switch# write (copies running-config over the startup-config, so when you restart the device it will use the last running configuration)

Switch#reload (restarts the device)

Switch#configure terminal (get into privileged exec mode)

I copied the whole lines, so you can see which mode you are entering the commands. (For example show running-config works at user-exec mode. If you write in any other modes it will not work)
There is also one exception for p.exec mode: You can put do in front of any command that you normally use in user exec like below, at whole works fine

Switch(config)#show running-config (do not work)
^
% Invalid input detected at '^' marker.
Switch(config)#do show running-config (works fine)
Building configuration...

Current configuration : 1295 bytes
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
.
.
.
.

