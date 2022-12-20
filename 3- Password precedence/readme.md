Before starting I need to tell you that these labs were designed assuming you already know the related topic and have checked the earlier labs, and what we will be testing or checking is the one in the header.
In this lab, I already handled the Telnet config (in the following labs we will check Telnet&SSH together) on the switch for remote testing. We will test different types of password commands. (Like after resetting the device, from console connection, telnet)
You can check the CLI modes to understand where these passwords can be set, from the 1st lab description (CLI user level&modes). Here are the options where you can set passwords.

1- Switch(config)#line console 0
Switch(config-line)#password linepass
Switch(config-line)#login *(if you use login local – it will override the password you put on the console line, and uses the username&password commands you set below.
write exit to go previous p.exec mode.
2- Switch(config)#username memo password userpass * (in line console or  vty lines (lines for SSH&telnet) if you write login local it will overwrite the login (on the running config)  and use the passwords used here -p.exec.mode)
You can also set more username&password combination. *(just be sure that passwords are case sensitive and usernames are not
3- Switch(config)#enable password enpass
4- Switch(config)#enable secret ensec
5- Switch(config)#do wr (for writing run.cfg to start.cfg)
Now we can do some tests after restarting the machine at user exec.
Switch#reload
Proceed with reload? [confirm]

After restart click the laptop/desktop/terminal – use default settings and press ok.
1&2 passwords set is related about after restart, 3&4 is related about going into user exec mode.
You will see that ensec overrides enpass, login local overrides line console password.
If you want to use the other you should disable the command from the config line by putting no infront of it:
Switch(config)#no enable secret
To cancel the local password (for console) you can write
Switch(config-line)#no login local
Switch(config-line)#login (actually just by writing login, local passwords is cancelled, may be it is just packet tracer – you can check the running config to be sure that only login is active at line console 0)
6- Switch(config)#line vty 0 15
      Switch(config-line)#password vtypass
      Switch(config-line)#login 
      (or)
      Switch(config-line)#login local
To test Telnet password, click PC/dekstop/command prompt – it takes you to cmd line
C:\>telnet 192.168.1.250 (this is the IP address I set for the switch)
Trying 192.168.1.250 ...Open
User Access Verification
Username: memo (because I used login local at VTY lines, you need to enter local user&pass combination)
Password: 
Switch>



