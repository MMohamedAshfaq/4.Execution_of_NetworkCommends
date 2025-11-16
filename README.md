# EXECUTION OF NETWORK COMMENDS
## Name : M.Mohamed Ashfaq
## Reg no: 212224240090
## AIM :
Use of Network commands in Real Time environment
## Software : 
Command Prompt And Network Protocol Analyzer
## Procedure: 
### To do this EXPERIMENT- follows these steps:

1. In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
2. All commands related to Network configuration which includes how to switch to privilege mode and normal mode and how to configure router interface and how to save this configuration to flash memory or permanent memory.

  This commands includes

    • Configuring the Router commands
    • General Commands to configure network
    • Privileged Mode commands of a router 
    • Router Processes & Statistics
    • IP Commands
    • Other IP Commands e.g. show ip route etc.

## Program
### Client
```
import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    ip = input("Enter website to ping: ")
    s.send(ip.encode())
    print(s.recv(1024).decode())

```
### Server
```
import socket
from pythonping import ping

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)
print("Server running... waiting for connection")

c, addr = s.accept()
print("Client connected:", addr)

while True:
    hostname = c.recv(1024).decode()
    try:
        result = str(ping(hostname, verbose=False))
        c.send(result.encode())
    except Exception as e:
        c.send(f"Error: {str(e)}".encode())
```


## Output
### Client & Server:
<img width="2522" height="1322" alt="4ex" src="https://github.com/user-attachments/assets/b67f4c81-11c7-4306-9778-c0c692c66266" />


## netstat
<img width="1280" height="1166" alt="4 1" src="https://github.com/user-attachments/assets/b0f6d156-7d25-42e9-bd99-9dc552f65dfc" />
<img width="1562" height="1122" alt="4 2" src="https://github.com/user-attachments/assets/6a04a411-93aa-4df4-a4fa-ce7ba3a5ae96" />


## ipconfig
<img width="1404" height="1046" alt="4 3" src="https://github.com/user-attachments/assets/1ff09732-d817-4c01-99f2-ceac84dc7864" />

## ping 
<img width="1646" height="970" alt="4 4" src="https://github.com/user-attachments/assets/10bcdad2-90b2-4377-a76c-c5756ab85e58" />

## tracert
<img width="1284" height="514" alt="4 5" src="https://github.com/user-attachments/assets/5167f79c-38b1-4bc5-aa91-8e415c9ed3de" />

## nslookup
<img width="758" height="112" alt="4 6" src="https://github.com/user-attachments/assets/a96109e0-3ea7-4f13-8f07-2cd3e5635dc4" />

## getmac
<img width="1186" height="294" alt="4 7" src="https://github.com/user-attachments/assets/18ee7e6f-c7a7-4a7c-82f3-463c4a875260" />

## hostname
<img width="842" height="86" alt="4 8" src="https://github.com/user-attachments/assets/c3e06afb-6eb7-4d6f-b3d5-19cf864ac569" />

## nbtstat
<img width="1498" height="842" alt="4 9" src="https://github.com/user-attachments/assets/889ffe24-922c-4d22-bcd2-63eca39059bc" />

## arp
<img width="1370" height="982" alt="4 10" src="https://github.com/user-attachments/assets/c57268e0-17f7-4b56-bd07-0af7c43d3be4" />

## systeminfo
<img width="1720" height="1176" alt="4 11" src="https://github.com/user-attachments/assets/08a6a6b8-1a4d-40a1-9516-a054367fadb6" />


## Result
Thus Execution of Network commands Performed
