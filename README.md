# 3c.CREATION FOR FILE TRANSFER USING TCP SOCKETS
## AIM
To write a python program for creating File Transfer using TCP Sockets Links
## ALGORITHM:
1. Import the necessary python modules.
2. Create a socket connection using socket module.
3. Send the message to write into the file to the client file.
4. Open the file and then send it to the client in byte format.
5. In the client side receive the file from server and then write the content into it.
## PROGRAM
= file.read()
    conn.send(data).encode()
Server.py:
```
import socket

host = '127.0.0.1'
port = 6000

server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server_socket.bind((host, port))
server_socket.listen(1)

print("Server waiting for connection...")
conn, addr = server_socket.accept()
print("Connected to:", addr)

filename = "sample.txt"

with open("DOC.txt", "rb") as file:
data
print("File sent successfully")
conn.close()
server_socket.close()
```
Client.py:
```
import socket

host = '127.0.0.1'
port = 6000

client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client_socket.connect((host, port))

with open("DOC1.txt", "wb") as file:
    while True:
        data = client_socket.recv(1024)
        if not data:
            break
        file.write(data)
print("File received successfully")
client_socket.close()
```
## OUPUT
Server.py:

<img width="1433" height="64" alt="Screenshot 2026-02-20 104818" src="https://github.com/user-attachments/assets/ba06ee87-723d-46eb-b319-d3e0901808b9" />

Client.py:

<img width="1426" height="236" alt="Screenshot 2026-02-20 104905" src="https://github.com/user-attachments/assets/4baa7663-5d67-43ac-ba24-548bcc35fed9" />

Source File:

<img width="819" height="622" alt="Screenshot 2026-02-20 104956" src="https://github.com/user-attachments/assets/d16474df-aeb1-4c43-8415-fc52468c7d03" />

Destination File:

<img width="813" height="605" alt="Screenshot 2026-02-20 105121" src="https://github.com/user-attachments/assets/4469f74e-282c-463a-8475-aedbf9847e82" />


## RESULT
Thus, the python program for creating File Transfer using TCP Sockets Links was 
successfully created and executed.
