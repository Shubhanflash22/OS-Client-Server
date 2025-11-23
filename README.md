# Client-Server System in C 💻🔗

A POSIX-compliant client-server application developed in C for efficient message passing, logging, and concurrent client operations.

## Table of Contents

* [Project Overview](#project-overview)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Implementation](#implementation)
* [Results](#results)
* [Future Work](#future-work)
* [License](#license)

## Project Overview

This project implements a multithreaded client-server system in C that allows multiple clients to communicate with a server using stateless communication. The server handles requests concurrently from multiple clients, providing functionalities like registration, request handling, response, and unregistration.

Key components include:

* POSIX-compliant C implementation.
* Inter-process communication using shared memory.
* Synchronization using pthread mutex for multithreaded server operations.
* Logging and monitoring of client-server interactions.

## Features

* **Stateless Communication:** Clients can register, send requests, receive responses, and unregister.
* **Concurrent Operations:** Multithreaded server with synchronized shared memory ensures multiple clients can operate simultaneously.
* **Interactive Client Menu:** Clients can interact through a menu with options for sending requests and unregistering.
* **Logging:** Maintains logs for all intermediate states and summarizes registered clients and requests serviced.

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/client-server-c.git
cd client-server-c

# Compile the server and client programs
gcc -pthread server.c -o server
gcc -pthread client.c -o client
```

## Usage

1. Start the server:

```bash
./server
```

2. Start one or more clients:

```bash
./client
```

3. Use the interactive menu in the client to register, send requests, or unregister.
4. Check the server console/logs to monitor client interactions and request handling.

## Implementation

* **Server:** Multithreaded using pthreads, synchronized with mutex in shared memory.
* **Client:** Single-threaded, menu-driven interface for user interaction.
* **Inter-process Communication:** Shared memory used to exchange messages between server and clients.
* **Logging:** Tracks registration, requests, responses, and summary statistics.

## Results

* Successfully implemented a multithreaded server handling multiple clients concurrently.
* Enabled stateless communication with detailed logging and monitoring.
* Interactive client interface simplifies testing and demonstration of system functionalities.

## Future Work

* Add support for authentication and secure communication.
* Enhance server to handle large-scale client operations efficiently.
* Implement persistent storage for logs and request history.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
