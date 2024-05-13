# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
client:
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',5000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
server:
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',5000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
![Screenshot 2024-05-13 091836](https://github.com/Ettasupraja/3b_CHAT_USING_TCP_SOCKETS/assets/151641352/861e1d04-527a-414d-b772-e0fd6c87c62f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
