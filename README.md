# Diffie-Hellman-Key-exchange-algorithm-implementation
Diffie Hellman Key exchange algorithm : Python implementation

Hi, this an implementation of Diffie-Hellman key exchange algorithm. It can be used to reach at a common secret key between two known persons or applications without any requirement of the secret key being sent over a network or email.

Steps to execute:

DHKE_SERV.py - This is the server module that listens to incoming connections from client. We need to pass two parameters before we can use it i.e. server_ip and port number.

e.g., DHKE_main('127.0.0.1',8844)

DHKE_CLI.py - This is the client module that negotiates the secret key with the DHKE server (DHEK_SERV.py). We need to pass the following parameters before we can start communicating with a DHKE server:

e.g., DHKE_CLI('127.0.0.1','192.168.1.3',8844)

  a) Server_ip - IP where the DHKE_SERV.py is running.
  b) Client_ip - IP from where you want to negotiate a key with the server.
  c) port_no   - Port no at which you have set the server module to run.

Server(DHEK_SERV) can store client keys for multiple client locations. A file named 'Client.keys' will be created to store the keys pinned to the respective the client_ips.
Client (DHKE_CLI) can only store one key that it has negotiated with the server in a file named 'agent.key'.
First, run the DHKE_SERV.py using a python IDE or compiler. Then use the DHKE_CLI.py with proper inputs to negotiate keys.
Intention behind these two modules were to enable multiple clients to communicate with a centralized server in secure fashion using their respective secret keys.

#Built by - Pritam Rakshit - 15/03/2017
