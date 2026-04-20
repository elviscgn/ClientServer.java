# Robot Worlds: Socket Programming Guide
This project serves as an introductory example of TCP Socket communication in Java. It demonstrates how two separate programs can talk to each other over a network.

## Prerequisites and Setup
To run this project, you will need two separate terminal windows open.

1. Compile the source code:
   `javac Client.java Server.java`

2. Start the Server:
   `java Server`
   (The server must be running first so it can "listen" for the client).

3. Start the Client:
   `java Client`

---

## Core Concepts for Beginners

### 1. The Socket Connection
A "Socket" is like a telephone jack. For a conversation to happen, one side must be waiting for a call (the Server), and the other side must know the number to dial (the Client).

* Port: We use port 6969. Think of this as a specific "extension number" on a phone system. Both the Client and Server must use the same port to find each other.
* IP Address: The Client uses 127.0.0.1, which is the "loopback" address. This tells the computer to look for the server on the same machine rather than out on the internet.

### 2. Data Streams
Computers send data in "streams." 
* DataOutputStream: Used by the Client to "pour" data into the connection.
* DataInputStream: Used by the Server to "collect" that data from the connection.

### 3. The Communication Loop
* The Client waits for you to type a message in the terminal.
* Once you hit Enter, it sends that text to the Server using UTF-8 encoding.
* The Server stays in a "while" loop, constantly checking if new data has arrived.
* Termination: The connection remains open until the Client sends the specific string "Over". This triggers both programs to close their streams and exit.

---

## Troubleshooting
* Connection Refused: Ensure the Server is running before you start the Client.
* Port in Use: If you get an error saying the port is already bound, it means another program (or a previous instance of your server) is still using port 6969. Close all terminal windows and try again.