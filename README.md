# So you want to do 401 JS without switching over to Mac/Linux? 
Don't be like me and inflict random hassles onto yourself when 401 is already challenging enough on it's own. Just actually use a mac or a machine running linux like the school suggests or better yet, dual boot. But if you're bound and determined to do it with a windows machine, it can be done...it's just going to be annoying. Here's how: 

## What you need to know
+ In the "create-a-chatroom" assignment, you will need to download something called [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) & enable [Windows Telnet](https://kb.ctera.com/article/how-to-open-a-telnet-session-on-windows-7-or-windows-8-os-16.html) in order to test your chat server. Windows Telnet is pretty much the worst (it has this initial configuration that enters one keystroke at a time so it's basically unusable and you feel like you're caught in the Matrix) so you have to use PuTTY with Telnet in order to do anything. Enter the correct configuration into PuTTY (your hostname, port, then select Telnet as the connection type). Do yourself a favor and set this config as a saved session because you will be opening and closing this thing a lot. 
+ HTTPie is hard to install without some help or reading multiple StackOverflows and watching Youtube. Just skip it and use curl and/or Postman to test HTTP req/res to your APIs.
+ Mongo: You'll need to follow these instructions: https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/. For some reason, Mongo's site where you can download Mongo doesn't give you instructions, it just assumes you somehow know to look for this and/or you are a wizard? /

