# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
Server.py
```
import socket
s=socket.socket()
s.bind(('localhost',9999))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMsg=c.recv(1024).decode()
    c.send(ClientMsg.encode())
```
Client
```
import socket
s=socket.socket()
s.connect(('localhost',9999))
while True:
    msg=input("Client> ")
    s.send(msg.encode())
    print("Server> ",s.recv(1024).decode())
```
## OUPUT
Server

<img width="632" height="309" alt="image" src="https://github.com/user-attachments/assets/95377535-704c-43aa-85db-a8a988325841" />

Client

<img width="590" height="251" alt="image" src="https://github.com/user-attachments/assets/9e87e5bd-79e0-4d7d-b92b-294fb98f265c" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
