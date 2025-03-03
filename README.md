# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
SERVER
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
```
CLIENT
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Moulidharan S, 212224240095')
    print(f'Received: {s.recv(1024)!r}')
```

## OUTPUT:
![server sshot](https://github.com/user-attachments/assets/2b7cae2f-05a8-4947-a383-20ecf50731ac)

![client sshot](https://github.com/user-attachments/assets/08c3af36-4325-4463-a507-b291300f76a6)








## RESULT:
The program is executed successfully
