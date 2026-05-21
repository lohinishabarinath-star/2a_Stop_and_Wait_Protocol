# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
##SERVER
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
##CLIENT
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~


## OUTPUT
##SERVER


<img width="810" height="212" alt="Screenshot 2026-05-21 122334" src="https://github.com/user-attachments/assets/3d6a3cd7-0f29-4efd-bd67-927d6d1548d8" />


##CLIENT


<img width="947" height="151" alt="Screenshot 2026-05-21 122352" src="https://github.com/user-attachments/assets/d73d12bd-7c98-404d-9442-9fe21af2c8bb" />


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
