import socket

s = socket.socket()
host = socket.gethostname()
port = 8080

try:
    s.connect((host, port))
    print('Connected to server')

    while True:
        incoming_message = s.recv(1024)
        incoming_message = incoming_message.decode()
        print('Server:', incoming_message)

        message = input('>> ')
        message = message.encode()
        s.send(message)
        print('Sent')
except ConnectionRefusedError:
    print('Connection refused. Make sure the server is running.')
except Exception as e:
    print('An error occurred:', e)
finally:
    s.close()
