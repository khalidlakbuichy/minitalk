# Minitalk Project

## Overview

The Minitalk project is part of the 42 network curriculum, focusing on inter-process communication (IPC) in Unix-based systems. The goal is to create a small data exchange program using Unix signals for communication between a client and a server.

## Concepts Learned

### Inter-Process Communication (IPC)

* **Signals**: Learning how to use Unix signals to send and receive information between processes.
* **Signal Handling**: Implementing custom signal handlers to manage communication.

### Client-Server Architecture

* **Client-Server Model**: Understanding and implementing the basics of a client-server architecture.
* **Data Transmission**: Efficient techniques for encoding and decoding messages sent via signals.

### Unix Programming

* **System Calls**: Using system calls like `kill` and `signal` to manage process communication.
* **Process Management**: Handling multiple processes and ensuring proper synchronization.

## Project Description

**Minitalk**: The project consists of two programs - a client and a server.

- **Server**: Waits for connections from clients and displays the messages received.
- **Client**: Sends messages to the server using Unix signals.

### Server

- Listens for incoming signals from the client.
- Reconstructs and displays the messages sent by the client.

### Client

- Sends a string message to the server, one character at a time, using signals.
- Encodes each character into a series of bits and sends them using the `SIGUSR1` and `SIGUSR2` signals.

## Implementation

* **Signal Encoding**: Encoding characters into bits and sending them as signals.
* **Signal Decoding**: Receiving signals and reconstructing the original message.
    
## Compilation and Execution

```bash
git clone https://github.com/khalidlakbuichy/minitalk.git
```
```bash
cd minitalk
```
```bash
make
```
```bash
./server
```
```bash
./client <server_pid> "message"
```
## Lessons Learned

* **Signal-Based IPC**: Implementing inter-process communication using Unix signals.
* **Client-Server Communication**: Developing a basic client-server model.
* **Unix System Programming**: Gaining experience with Unix system calls and signal handling.

## Conclusion

The Minitalk project provided valuable insights into inter-process communication, client-server architecture, and Unix system programming, essential for building robust and efficient applications in a Unix environment.
