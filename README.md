# yowsup-commandserver
yowsup layer that auto execute commands using whatsapp.

## Installation

Install [yowsup](https://github.com/tgalal/yowsup/tree/develop) from the develop branch. (This is created for version 2.4.48)

After installing yowsup. Install this extension running:
```
python setup.py install
```
Modify the file layer.py to add an allowed client. Modify the line:

	allowed_users = ['34666888999@s.whatsapp.net']
	
And add your user id. If you have no idea of wich user you have, execute the demo application and check the error message at the console when you send a whatsapp to the server.

## Execution

To launch yowsup as a command server, from the folder where the file "yowsup-cli" exists, execute: 

	python yowsup-cli demos --config <file.config> --commandserver
	
where "file.config" is a file where the whatsapp credentials are, as in other examples of yowsup. Something like:

	cc=39
	phone=39XXXXXXXX
	password=c5NWTzOrsgCRQr77Yhwafdj+Tgg=


## Allowing new commands

When it works, modify the layer.py to add all allowed commands you want. If a command needs sudo rights (as "reboot" in the code) you must execute yowsup with sudo or root user if the commands needs admin rights.






