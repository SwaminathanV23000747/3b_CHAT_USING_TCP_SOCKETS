# 3b.CREATION FOR CHAT USING TCP SOCKETS
# AIM:
To write a python program for creating Chat using TCP Sockets Links.
# ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
# PROGRAM:
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
# OUPUT:
## Client:
![313481878-b8a7755e-6608-4fa2-a4f6-e2df917dfac9](https://github.com/820NaveenKumar208/3b_CHAT_USING_TCP_SOCKETS/assets/154746066/3b201be5-286e-4c0c-8850-196d6fc63d19)
## Server:
![313481844-92fb00d4-a7f8-4792-8058-adff7ebe7214](https://github.com/820NaveenKumar208/3b_CHAT_USING_TCP_SOCKETS/assets/154746066/0adf18e4-39c9-47c3-ab12-b565672b312d)

# RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
