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
#server
```
import socket
HOST , PORT = '127.0.0.1',65432
with socket.create_server((HOST,PORT)) as s:
    conn , addr = s.accept()
    with conn:
        print(f'connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
#client
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Thenukishore, 2122223100059')
    print(f'Received: {s.recv(1024)!r}')
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/cae22325-1bdc-4ab4-a8e9-8dd02c9b8328)

## RESULT:
The program is executed successfully
