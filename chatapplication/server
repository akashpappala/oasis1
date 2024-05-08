import socket
s = socket.socket()
host = socket.gethostname()
print('Server will start on host:', host)
port = 8080
s.bind((host, port))
print('Waiting for connection...')

s.listen(1)
conn, addr = s.accept()
print('Received connection from:', addr)

while True:
    message = input('>> ')
    message = message.encode()
    conn.send(message)
    print('Sent')
    incoming_message = conn.recv(1024)
    incoming_message = incoming_message.decode()
    print('Client:', incoming_message)
