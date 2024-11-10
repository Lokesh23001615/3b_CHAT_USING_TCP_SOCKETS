# 3b.CREATION FOR CHAT USING TCP SOCKETS
# Name: Lokesh M
# Reg no: 212223230114
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client.py 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
  msg=input("Client > ")
  s.send(msg.encode())
  print("Server > ",s.recv(1024).decode())
```

## server.py
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
## OUPUT
## client.py
![image](https://github.com/user-attachments/assets/7202e539-343a-459e-be92-5afc1cf163a0)

## server.py
![image](https://github.com/user-attachments/assets/52396f1e-b6e4-4105-be74-698fb7098993)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
