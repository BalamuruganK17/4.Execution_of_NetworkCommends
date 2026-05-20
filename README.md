# 4.Execution_of_NetworkCommands
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

## PROGRAM:
## CLIENT:
```
client.py
import socket
from pythonping import ping
s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True: hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```
## SERVER:
```
server.py

import socket s=socket.socket() s.connect(('localhost',8000)) while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```
## Output:
## NETSTAT
<img width="1917" height="903" alt="Screenshot 2026-05-20 151839" src="https://github.com/user-attachments/assets/d51fe2c8-725a-410d-8809-a6af800fab88" />
## IP CONFIGURATION
<img width="1898" height="899" alt="Screenshot 2026-05-20 151855" src="https://github.com/user-attachments/assets/3baf02b5-939c-48b4-b23b-ce2639ccba62" />
## GETMAC 
<img width="1781" height="370" alt="Screenshot 2026-05-20 151920" src="https://github.com/user-attachments/assets/88799d24-320f-46f1-a547-1a608e04796f" />
## ARP
<img width="1859" height="900" alt="Screenshot 2026-05-20 151933" src="https://github.com/user-attachments/assets/35f8c567-2172-44fb-97f2-a1c9dcfe11d2" />
## SYSTEM INFO
<img width="1892" height="904" alt="Screenshot 2026-05-20 151950" src="https://github.com/user-attachments/assets/54d734e9-ba69-49d8-a904-dfad44c34c6b" />
## NBTSTAT 
<img width="1706" height="851" alt="Screenshot 2026-05-20 152005" src="https://github.com/user-attachments/assets/e691e2b9-26d6-4747-a675-97466cd0a71f" />
## HOSTNAME
<img width="971" height="341" alt="Screenshot 2026-05-20 152105" src="https://github.com/user-attachments/assets/47187e00-89f2-44f1-a0cf-fc5e06195794" />
## NS LOOKUP
<img width="558" height="123" alt="Screenshot 2026-05-20 152126" src="https://github.com/user-attachments/assets/2b545129-7850-411c-8989-291b7849fa39" />
## PING
<img width="1050" height="753" alt="Screenshot 2026-05-20 152213" src="https://github.com/user-attachments/assets/0e5eded9-ae7a-4a9f-9a73-75e4be936292" />
## TRACET
<img width="1004" height="139" alt="Screenshot 2026-05-20 152221" src="https://github.com/user-attachments/assets/5c26092b-48b2-40f7-82ae-a9b98292db5f" />


## Result
Thus Execution of Network commands Performed 
