# Java Client-Server Socket Programming

A beginner-friendly Java networking project that demonstrates **TCP client-server communication using Java Socket Programming**.

The project consists of a client and a server that communicate with each other through a socket connection on **localhost using port 5000**.

---

## 📌 Project Overview

This project demonstrates how two Java applications can communicate over a network using **TCP sockets**.

The **Server** waits for a client connection. Once the client connects, it sends a message to the server. The server receives the message, displays it, and sends a response back to the client.

### Communication Flow

```text
Client                          Server
  |                               |
  |------ Connect to port 5000 -->|
  |                               |
  |------ "Hello Server" -------->|
  |                               |
  |<------- "Hello Client" -------|
  |                               |
  |---------- Close ------------->|
```

---

## ✨ Features

* TCP-based client-server communication
* Uses Java `Socket` and `ServerSocket`
* Sends messages from client to server
* Sends responses from server to client
* Uses input and output streams
* Demonstrates basic network programming
* Simple command-line execution
* Properly closes socket connections

---

## 🛠️ Technologies Used

* **Java**
* **Java Networking**
* **TCP/IP**
* `Socket`
* `ServerSocket`
* `BufferedReader`
* `InputStreamReader`
* `PrintWriter`

---

## 📂 Project Structure

```text
Java-Client-Server/
│
├── Server.java
├── Client.java
└── README.md
```

### `Server.java`

The server:

1. Creates a `ServerSocket` on port `5000`.
2. Waits for a client connection.
3. Accepts the client connection.
4. Receives a message from the client.
5. Displays the received message.
6. Sends a response to the client.
7. Closes the connection.

### `Client.java`

The client:

1. Connects to the server using `localhost` and port `5000`.
2. Sends `"Hello Server"`.
3. Waits for the server response.
4. Displays the response.
5. Closes the connection.

---

## ⚙️ Prerequisites

Before running the project, make sure **Java JDK** is installed.

Check the Java version:

```bash
java -version
```

Check the Java compiler:

```bash
javac -version
```

---

## ▶️ How to Run

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate to the project folder:

```bash
cd Java-Client-Server
```

---

### Step 2: Compile the Server

```bash
javac Server.java
```

### Step 3: Start the Server

```bash
java Server
```

You should see:

```text
Server started....
Waiting for Client....
```

---

### Step 4: Open a Second Terminal

Keep the server terminal running.

Open another terminal in the same project folder.

Compile the client:

```bash
javac Client.java
```

Run the client:

```bash
java Client
```

---

## 💻 Expected Output

### Server Output

```text
Server started....
Waiting for Client....
Client connected.
Client says: Hello Server
Connection closed.
```

### Client Output

```text
Connected to server.
Server says: Hello Client
Connection closed.
```

---

## 🔍 How It Works

### 1. ServerSocket

The server creates a `ServerSocket`:

```java
ServerSocket serverSocket = new ServerSocket(5000);
```

This makes the server listen for incoming client connections on port `5000`.

### 2. Accepting the Client

The server waits for a client using:

```java
Socket socket = serverSocket.accept();
```

The program pauses here until a client connects.

### 3. Sending Data

The client sends a message using `PrintWriter`:

```java
output.println("Hello Server");
```

### 4. Receiving Data

The server receives the message using `BufferedReader`:

```java
String message = input.readLine();
```

### 5. Sending a Response

The server sends a response:

```java
output.println("Hello Client");
```

### 6. Closing the Connection

Both sides close their socket connections after communication is complete.

---

## 🧠 Concepts Demonstrated

This project provides practical experience with:

* Client-server architecture
* TCP communication
* Socket programming
* Java networking
* `ServerSocket`
* `Socket`
* Input streams
* Output streams
* Exception handling
* Network ports
* `IOException`

---

## ⚠️ Important Notes

* The **server must be started before the client**.
* Both programs use port **5000**.
* The client connects to `localhost`, so both programs are running on the same computer.
* If port `5000` is already being used by another application, the server may fail to start.
* The current server handles **one client connection at a time**.

---

## 🚀 Future Improvements

This project can be extended by adding:

* Multiple client support
* Continuous messaging
* Two-way chat functionality
* Multi-threading
* Client usernames
* Message timestamps
* Server-side logging
* Network communication between different computers
* Graceful handling of client disconnections
* GUI using Java Swing

---

## 🎯 Learning Objective

The main objective of this project is to understand the fundamentals of **Java Socket Programming and TCP client-server communication**.

It provides a foundation for developing more advanced networking applications such as:

* Chat applications
* Multiplayer games
* File transfer applications
* Network-based services
* Distributed applications

---

## 📄 License

This project is created for **educational and learning purposes**.

Feel free to modify and improve the project for your own learning and development.
