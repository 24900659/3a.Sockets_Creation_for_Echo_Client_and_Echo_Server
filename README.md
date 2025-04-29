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
 client:
 
 import socket
 
 s=socket.socket()
 
 s.connect(('localhost',8000))
 
 while True:
 
 msg=input("Client > ")
 
 s.send(msg.encode())
 
 print("Server > ",s.recv(1024).decode())
 
  server:
  
 import socket
 
 s=socket.socket()
 
 s.bind(('localhost',8000))
 
 s.listen(5)
 
 c,addr=s.accept()
 
 while True:
 
 ClientMessage=c.recv(1024).decode()
 
 c.send(ClientMessage.encode())

## OUPUT
CLIENT:
![Screenshot (47)](https://github.com/user-attachments/assets/928bf6bd-d0a6-4f59-b2bf-015188380b6f)
SERVER:
![Screenshot (48)](https://github.com/user-attachments/assets/5c78f387-1333-4294-aa4d-9791ffc6f6bf)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
