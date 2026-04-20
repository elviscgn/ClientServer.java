# ClientServer.java
Simple example for Robot Worlds prep

## Usage
1. Compile the code:

```bash
javac Client.java
javac Server.java
```

2. Run the server in one terminal:

```bash
java Server
```

3. Run the client in another terminal:

```bash
java Client
```

The server will print the message received from the client, and the client will print the response from the server.

## Explanation
- The `ClientServer` class contains the main method which checks the command-line arguments to determine whether to run as a server or a client.
- The server listens on port 12345 for incoming connections and prints any messages received from clients.
- The client connects to the server on localhost at port 12345, sends a message, and waits for a response from the server before printing it.
- This example demonstrates basic socket programming in Java, allowing for communication between a client and a server using TCP sockets.

## Note
Make sure to run the server before the client, as the client needs to connect to the server. Also, ensure that the port number (12345 in this case) is not being used by another application on your machine.

