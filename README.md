TCP Proxy Server
This project implements a TCP Proxy Server in C++ using the epoll mechanism and a thread pool for efficient connection handling. The proxy server listens for incoming connections on a specified local IP and port, then forwards the traffic to a specified remote IP and port.

Features
Non-blocking I/O using epoll
Multi-threaded handling of client connections with a thread pool
Simple implementation without third-party networking libraries
Technologies Used
C++
epoll
threadpool
pthreads
Project Structure
proxy_server.cpp: Main implementation of the TCP Proxy Server
Makefile: Script to compile the C++ code
server.py: Simple Python server script for testing
client.py: Simple Python client script for testing
Compilation and Execution
Requirements
g++ compiler
make
Python 3
Compilation
Compile the proxy server using make:
make
Running the TCP Proxy Server
Ensure you have compiled the proxy_server executable.

Open a terminal and start the TCP Proxy Server with the following command:

./proxy_server <local_ip> <local_port> <remote_ip> <remote_port>
Example:

./proxy_server 127.0.0.1 8080 127.0.0.1 9090
Running the Test Server and Client
Open a new terminal and navigate to the project directory. Start the Python test server:

python3 server.py
Open another terminal and navigate to the project directory. Start the Python test client:

python3 client.py
The client will connect to the proxy server, which in turn will forward the traffic to the test server.
