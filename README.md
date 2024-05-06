# 4a.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PROGRAM
## CLIENT:
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
## SERVER:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
## OUTPUT
## PING COMMAND:
## CLIENT:
![325101129-3104feb5-6a1d-41bc-bcf1-88a451a6f2f2](https://github.com/DharanAditya/4.Execution_of_NetworkCommends/assets/147473834/7e72baee-5248-4046-9af5-39b7093b8fd2)


## SERVER:
![325101177-455acf80-50ec-4a8c-af04-fb9049018eaa](https://github.com/DharanAditya/4.Execution_of_NetworkCommends/assets/147473834/11c4e980-5b03-4cee-bcb5-36fdd58f10d2)


## TRACERT COMMAND:
![325101228-7c0aa54e-ccd4-4069-a0d7-9d684004875f](https://github.com/DharanAditya/4.Execution_of_NetworkCommends/assets/147473834/6de793df-2498-4c69-a39f-43e731417465)


## Result
Thus Execution of Network commands Performed.
