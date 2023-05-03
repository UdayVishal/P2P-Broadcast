# P2P-Broadcast
          Peer-to-peer messaging and broadcast message
The client-server application used in this project enables client-to-client communication without the aid of the server. The server is solely used to exchange contact details with customers that are currently active. Clients can connect to the server, log in with a password, and view the list of clients that are currently active. The remote client will be prompted to accept the new connection before they may choose any other active client to connect with. Once the connection is established successfully, clients can communicate with one another without the assistance of the server. In addition, a client can ask the server to send a message to all of the clients in its database. The broadcast message should reach every customer who will be online in the next 30 minutes.

Requirements
The application is written in C++, and it is designed to run on a Linux distribution. You will need to have the following installed on your machine.
* G++ compiler
* Oracle Virtual Box

Building the Project
The project can be built using the Makefiles included in the project directory. To build the project, run the following command:
“ Make all”
If you want to create a make file for both client and server, run the following command.
“ Make Client ”  “ Make Server ”

Running the Server Application
* To run the server application , we need to compile the file using g++ compiler and run the following command. “ g++ server.cpp -o server -pthread ”
* Server can be started by running the following command. “ ./server ”
* The server will listen on port 4400 and allow at least 50 connections simultaneously. 
* If there are more than 50 connections at some time, TCP will ignore the new connections, and clients will retry (automatically) at least 5 more times in the next 10 minutes.
<img width="365" alt="image" src="https://user-images.githubusercontent.com/86564176/235829324-685e4e66-07b3-44e7-a2f4-2d1300dd6a83.png">

Running the Client Application
* To run the client application, we need to compile the file using g++ compiler and run the following command. “g++ client.cpp -o client  -pthread ”
* Client can be started by running the following command. “ ./client <IP address> <port> ”.
<img width="434" alt="image" src="https://user-images.githubusercontent.com/86564176/235829348-1cd574b3-f1eb-46cf-aa70-56c2b5f7dc16.png">


 Peer to Peer Communication
* After establishing a connection with the server, a client can view a list of all currently active clients by choosing the relevant option. 
* The remote client will be prompted to accept the new connection before they may pick any other active client to connect with.
*  Once the connection is made, the clients can communicate with one another without the assistance of the server.
<img width="353" alt="image" src="https://user-images.githubusercontent.com/86564176/235829375-b37414a3-e45d-48a0-8121-19f13332bc4b.png">
<img width="429" alt="image" src="https://user-images.githubusercontent.com/86564176/235829398-215c2c9c-81c4-40cf-b2e9-9aecaa2c0d24.png">


Broadcast Message
* The server can be asked by a client to broadcast a message to all clients in its CSV file. 
* The broadcast message should reach every customer who will be online in the next 30 minutes. 
* Select the appropriate option from the menu, then type the message you want to broadcast.
<img width="416" alt="image" src="https://user-images.githubusercontent.com/86564176/235829428-782977a3-2b1e-4b14-a7bf-12a09476d73e.png">


 Libraries Used
* #include <arpa/inet.h>
* #include <netinet/in.h>
* #include <unistd.h>
* #include <pthread.h>
* #include <iostream>
* #include <cstring>
* #include <string.h>
* #include <cstring>
* #include <unistd.h>
* #include <netdb.h

Conclusion
This project shows how to use C/C++ and Linux to create a peer-to-peer messaging system and a broadcast message system. The server application offers a list of active clients and allows clients to authenticate themselves using a password. Clients can communicate with one another and transmit messages thanks to the client application. A client can send a message to every client in the database using the broadcast message mechanism.

