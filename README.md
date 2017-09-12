# So you want to do 401 JS without switching over to Mac/Linux? 
Don't be like me and inflict random hassles onto yourself when 401 is already challenging enough on it's own. Just actually use a mac or a machine running linux like the school suggests or better yet, dual boot. But if you're bound and determined to do it with a windows machine, it can be done...it's just going to be annoying. Here's how: 

## The Linux Subsystem
Your best bet is to install the Linux Subsystem on Windows. This allows you to use Linux on Windows without a lot of hassle. Also, Microsoft's own site with installation instructions is super confusing. Go ahead and make sure you've checked for updates to Windows recently and make sure you are using 64 bit. I believe it does not yet work on 32 bit? Instructions on how to figure that out [here](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide). You will also have to put your version of Windows into developer mode: 
(Open Settings -> Update and Security -> For developers).

Then...
+ Open PowerShell ISE (type Powershell ISE into your search bar), run it as an Admin (right click)
+ Copy in: Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux and run that
+ It will ask you to come up with a username/password, do that
+ Now you should have the Linux Subsystem installed, but then you have to make sure Linux is all good by doing: 
    + sudo apt update
    + sudo apt upgrade
+ Then I went ahead and installed NPM/Node using the 301 prework instructions for linux
+ Now install nvm
+ Bash may start at a weird spot, which you can fix by cd'ing to the right spot. cd /mnt/C/ will get you to your C drive, then navigate from there

## Installing Bcrypt with Linux Subsystem
We solved this problem by basically getting npm, node, nvm and gyp installed. In nvm, we upgraded to v8 of Node. That seemed to fix the problem but your mileage may vary.

## What if I can't get the subsystem to install? Here's what you need to know
+ In the "create-a-chatroom" assignment, you will need to download something called [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) & enable [Windows Telnet](https://kb.ctera.com/article/how-to-open-a-telnet-session-on-windows-7-or-windows-8-os-16.html) in order to test your chat server. Windows Telnet is pretty much the worst (it has this initial configuration that enters one keystroke at a time so it's basically unusable and you feel like you're caught in the Matrix) so you have to use PuTTY with Telnet in order to do anything. Enter the correct configuration into PuTTY (your hostname, port, then select Telnet as the connection type). Do yourself a favor and set this config as a saved session because you will be opening and closing this thing a lot. 
+ HTTPie is hard to install without some help or reading multiple StackOverflows and watching Youtube. Just skip it and use curl and/or Postman to test HTTP req/res to your APIs.
+ Mongo: You'll need to follow these instructions: https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/. For some reason, Mongo's site where you can download Mongo doesn't give you instructions, it just assumes you somehow know to look for this and/or you are a wizard? /
