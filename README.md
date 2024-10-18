# 3a                                                            CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# NAME:KARTHICK KISHORE T
# REGNO:212223220042
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
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT
![Screenshot 2024-10-04 105948](https://github.com/user-attachments/assets/b3d475e9-dc80-4633-b355-f297b9501933)

![Screenshot 2024-10-02 113727](https://github.com/user-attachments/assets/77020e46-47a0-4558-b52e-941231f2d6e4)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
