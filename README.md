# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
### SERVER:
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
## OUPUT:
### CLIENT:
![Screenshot 2024-04-03 113052](https://github.com/Rogith08/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/162728044/b6bde692-097c-44ed-b6f5-80ff0ad66974)


### SERVER:
![Screenshot 2024-04-03 113102](https://github.com/Rogith08/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/162728044/65606126-9378-44f4-9b10-45d0011498da)


## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
