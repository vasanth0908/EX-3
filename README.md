# EX-3:
IMPLEMENTATION OF SLIDING WINDOW PROTOCOL 
EXP: 3 DATE:22-03-2023
AIM : To write a python program to perform sliding window protocol ALGORITHM :

Start the program.

Get the frame size from the user

To create the frame based on the user request.

To send frames to server from the client side.

If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.

Stop the program CLIENT PROGRAM : import socket s=socket.socket() s.bind(('localhost',8000)) s.listen(5) c,addr=s.accept() size=int(input("Enter number of frames to send:")) l=list(range(size)) s=int(input("Enter Window Size:")) st=0 i=0 while True:

while(i<len(l)):

 st+=s
 c.send(str(l[i:st]).encode())
 ack=c.recv(1024).decode()
 if ack:
 	print(ack)
 	i+=s
SERVER PROGRAM : import socket s=socket.socket() s.connect(('localhost',8000)) while True: print(s.recv(1024).decode()) s.send("acknowledgement recieved from the server".encode())
OUPUT:
![1](https://github.com/vasanth0908/EX-3/assets/122000018/d6245344-48d9-4556-a451-78b9bf8077b7)

![2](https://github.com/vasanth0908/EX-3/assets/122000018/65060834-47b7-4b0c-a24a-e147d5f2e216)

RESULT:
IMPLEMENTATION OF SLIDING WINDOW PROTOCOL HAS BEEN EXCUTED SUCCESSFULLY
