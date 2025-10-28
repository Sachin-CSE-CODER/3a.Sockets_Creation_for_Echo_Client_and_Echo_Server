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
### Client

```
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```

### Server

```
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
<img width="621" height="126" alt="Screenshot 2025-10-28 085403" src="https://github.com/user-attachments/assets/68c20032-ea05-419a-877a-41f8849d4aef" />
<img width="623" height="222" alt="Screenshot 2025-10-28 085353" src="https://github.com/user-attachments/assets/cbbd3f35-197d-4e6d-8c12-3caa200cf387" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
