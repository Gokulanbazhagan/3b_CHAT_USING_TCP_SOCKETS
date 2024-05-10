# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
   
## PROGRAM:
Developed by: GOKULARAMANAN K

Register Number: 212222230040

## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

## Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```

## OUPUT:
![image](https://github.com/anbuvinotha/3b_CHAT_USING_TCP_SOCKETS/assets/144871822/46e88afd-5408-45d9-af8e-0f2f11de49f5)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
