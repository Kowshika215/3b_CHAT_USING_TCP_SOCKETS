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
##client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
##server
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
##Client
![Screenshot 2025-05-10 134500](https://github.com/user-attachments/assets/6d9faf48-c3d1-497e-a670-bf6a0d282a5d)
##Server
![Screenshot 2025-05-10 134510](https://github.com/user-attachments/assets/0900ffd6-e197-49be-bb9f-938159191e10)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
