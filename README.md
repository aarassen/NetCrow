
# NetCrow - by Raspberryy

This is a fun little Tool made for the Raspberry Pi!

But of course it can be used on every Linux System... <br />
It is using python Code to execute the MiTM automatically. <br />
The Attack itself is using ettercap to analyize Network Traffic. <br />

The main Features are:
 - Automatic start at Boot (if needed)
 - Sending gathered Data via E-Mail to the User
 - Autosaving 

# 1 Installing NetCrow
  sudo -i <br />
  cd to/path/you/want/to/install <br />
  git clone https://github.com/Raspberryy/NetCrow.git <br />
  cd NetCrow/ <br />
  sh install.sh <br />
  
# 2 Enable IP IpTables
  sudo nano /etc/etter.conf<br />
  
    Search for "redir_command_on/off" <br />
    Remove # from "redir_command_on = "iptables [...]""<br />
    Remove # from "redir_command_off = "iptables [...]""<br />

 
# 3 Configure E-Mail Sending
  nano attack.py
    
    Enter your E-Mail Data:
    Sender = "YourGmailAdress@gmail.com"
    Password = "YourGMailPassword"
    Reciever = "YourEMailAdress@anyhost.com"

  DO NOT FORGET: <br />
    Allow less secure apps to access your Gmail account <br />
    Info: https://support.google.com/accounts/answer/6010255?hl=en <br />
    Disable: https://www.google.com/settings/security/lesssecureapps

# Installing Automatic Boot (Only if needed)
  sudo python AutoStart.py

 
