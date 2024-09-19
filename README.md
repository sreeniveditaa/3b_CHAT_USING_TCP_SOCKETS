# 3b.CREATION FOR CHAT USING TCP SOCKETS
# DATE : 
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
Developed by: SREE NIVEDITAA SARAVANAN
Reg no: 212223230213
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
### Server
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
### Client
![{862EBF83-B711-4FC4-9B8C-D1FD2F762277}](https://github.com/user-attachments/assets/72c6979f-b3f9-4116-a494-8cde2f8fcc6c)

### Server
![{3A45037C-16B5-4EC4-A025-6A4ABB8452B7}](https://github.com/user-attachments/assets/d0da286b-e25a-4705-9d05-a011cef3e231)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
